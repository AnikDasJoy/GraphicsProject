#include<windows.h>
#include<GL/glut.h>
#include<math.h>
# define PI 3.14159



void night(int);
void displayBack(int);
void display();
void day();
void nightView();

float _move3 = 0.0f;
float _movef = 0.0f;
float _movefb = 0.0f;
GLfloat position = 0.0f;
GLfloat position2 = 0.0f;
GLfloat position3 = 0.0f;
GLfloat position4 = 0.0f;
GLfloat speed = 0.1f;




void updateauto(int value) {


    _move3 += .005;
    if(_move3-1.663  > 1.0)
    {
        _move3 = -1.0;
    }

      _movef += .01;
    if(_movef-1.3 > 1.0)
    {
        _movef = -1.0;

    }
    _movefb -= .01;
    if(_movefb+1.3 < -1.0)
    {
        _movefb = 1.0;

    }

	glutPostRedisplay();
	glutTimerFunc(20, updateauto, 0);
}
///




void update(int value) {
    if(position <-2.0)
        position = 2.0f;
    position -= speed;
	glutPostRedisplay();
	glutTimerFunc(100, update, 0);
}



void update2(int value) {
    if(position2 >2.0)
        position2 = -2.0f;
    position2 += speed;
	glutPostRedisplay();
	glutTimerFunc(100, update2, 0);
}

void update3(int value) {
    if(position3 >2.0)
        position3 = -2.0f;
    position3 += speed;
	glutPostRedisplay();
	glutTimerFunc(100, update3, 0);
}

void update4(int value) {
    if(position4 <-1)
        position4 = -0.;
    position4 -= speed;
	glutPostRedisplay();
	glutTimerFunc(100, update4, 0);
}



void idle()
{
    glutPostRedisplay();
}
void init()
{
   glClearColor(0.0f, 0.0f, 0.0f, 1.0f);
}



 void SpecialInput(int key, int x, int y){
     switch(key){


case GLUT_KEY_LEFT:
  glutTimerFunc(100, update, 0);
    break;

case GLUT_KEY_RIGHT:
    glutTimerFunc(100, update2, 0);

    break;


}

glutPostRedisplay();
}



void handleKeypress(unsigned char key,int x,int y)
{
    switch(key){
case 'd':

    glutDisplayFunc(day);
    glutPostRedisplay();
    break;

case 'n':

     glutDisplayFunc(nightView);
    glutPostRedisplay();
    break;

    case 'b':

      speed=0.1;
    glutPostRedisplay();
    break;


    }

}


void displayBack(int value)
{
    glutDisplayFunc(display);
}

void nightView()
{
    glClearColor(1,1,1,1);
	glClear(GL_COLOR_BUFFER_BIT);


     float x,  y,  radius,triangleAmount,twicePi;

//SKY / MOON / CLOUD
{


    //SKY
    glBegin(GL_QUADS);
    glColor3ub(255,255,255);
    glVertex2f(-1,1);
    glVertex2f(-1,.03);
    glVertex2f(1,.03);
    glVertex2f(1,1);
    glEnd();
    glBegin(GL_QUADS);
    glColor3ub(94,94,94);
    glVertex2f(-1,1);
    glVertex2f(-1,.05);
    glVertex2f(1,.05);
    glVertex2f(1,1);
    glEnd();
    glBegin(GL_QUADS);
    glColor3ub(41,49,51);
    glVertex2f(-1,1);
    glVertex2f(-1,.14);
    glVertex2f(1,.14);
    glVertex2f(1,1);
    glEnd();



      //Moon
    {

         //1st round effect
    {
        int i;
	GLfloat x=-.2f; GLfloat y=.91f; GLfloat radius =.22f;
	int triangleAmount = 20;
	GLfloat twicePi = 2.0f * PI;

	glBegin(GL_TRIANGLE_FAN);
    glColor3ub(53, 60, 62);
    glVertex2f(x, y);
    for(i = 0; i <= triangleAmount;i++){
        glVertex2f(
            x + (radius * cos(i *  twicePi / triangleAmount)),
            y + (radius * sin(i * twicePi / triangleAmount))
        );
    }
	glEnd();
    }

         //2nd round effect
    {
        int i;
	GLfloat x=-.2f; GLfloat y=.91f; GLfloat radius =.19f;
	int triangleAmount = 20;
	GLfloat twicePi = 2.0f * PI;

	glBegin(GL_TRIANGLE_FAN);
    glColor3ub(61, 66, 73);
    glVertex2f(x, y);
    for(i = 0; i <= triangleAmount;i++){
        glVertex2f(
            x + (radius * cos(i *  twicePi / triangleAmount)),
            y + (radius * sin(i * twicePi / triangleAmount))
        );
    }
	glEnd();
    }


        //3rd round effect
    {
        int i;
	GLfloat x=-.2f; GLfloat y=.91f; GLfloat radius =.13f;
	int triangleAmount = 20;
	GLfloat twicePi = 2.0f * PI;

	glBegin(GL_TRIANGLE_FAN);
    glColor3ub(81, 85, 90);
    glVertex2f(x, y);
    for(i = 0; i <= triangleAmount;i++){
        glVertex2f(
            x + (radius * cos(i *  twicePi / triangleAmount)),
            y + (radius * sin(i * twicePi / triangleAmount))
        );
    }
	glEnd();
    }
     //main
    {
    int i;
	GLfloat x=-.2f; GLfloat y=.91f; GLfloat radius =.07f;
	int triangleAmount = 20;
	GLfloat twicePi = 2.0f * PI;

	glBegin(GL_TRIANGLE_FAN);
    glColor3ub(235, 237, 237);
    glVertex2f(x, y);
    for(i = 0; i <= triangleAmount;i++){
        glVertex2f(
            x + (radius * cos(i *  twicePi / triangleAmount)),
            y + (radius * sin(i * twicePi / triangleAmount))
        );
    }
	glEnd();

    }

    }



    //STAR
    {


    glPointSize(2.0f);
    glBegin(GL_POINTS);
    glColor3ub(255,255,255);
//-----------------------
    glVertex2f(-.95,.7);
    glVertex2f(-.9,.65);

    glVertex2f(-.8,.75);

    glVertex2f(-.7,.7);
    glVertex2f(-.6,.72);

    glVertex2f(-.5,.67);
    glVertex2f(-.4,.73);

    glVertex2f(-.3,.68);
    glVertex2f(-.2,.7);

    glVertex2f(-.1,.74);
    glVertex2f(-.9,.79);

    //-----------------

    glVertex2f(-.95,.6);
    glVertex2f(-.9,.65);

    glVertex2f(-.8,.55);

    glVertex2f(-.7,.62);
    glVertex2f(-.6,.52);

    glVertex2f(-.5,.6);
    glVertex2f(-.4,.63);

    glVertex2f(-.3,.66);
    glVertex2f(-.2,.89);

    glVertex2f(-.8,.9);
    glVertex2f(-.5,.85);

    //------------------

    glVertex2f(.95,.7);
    glVertex2f(.9,.65);

    glVertex2f(.8,.75);

    glVertex2f(.7,.7);
    glVertex2f(.6,.72);

    glVertex2f(.5,.67);
    glVertex2f(.4,.73);

    glVertex2f(.3,.68);
    glVertex2f(.2,.7);

    glVertex2f(.1,.74);
    glVertex2f(.9,.79);

    //-----------------

    glVertex2f(.95,.6);
    glVertex2f(.9,.65);

    glVertex2f(.8,.55);

    glVertex2f(.7,.62);
    glVertex2f(.6,.52);

    glVertex2f(.5,.6);
    glVertex2f(.4,.63);

    glVertex2f(.3,.66);
    glVertex2f(.2,.89);

    glVertex2f(.8,.9);
    glVertex2f(.5,.85);


    //---------------


    glVertex2f(.7,.95);
    glVertex2f(.8,.95);

    glVertex2f(.75,.82);
    glVertex2f(.65,.92);

    glVertex2f(.07,.95);
    glVertex2f(.18,.95);

    glVertex2f(.0,.92);
    glVertex2f(-.07,.92);

    glVertex2f(.0,.82);
    glVertex2f(-.07,.72);


    glVertex2f(-.7,.95);

    glVertex2f(-.8,.95);

    glVertex2f(-.75,.82);
    glVertex2f(-.65,.92);


    glEnd();
    }

}


{

    //Flag
{




     //FLAG QUAD  2
    glBegin(GL_QUADS);
    glColor3ub(178,34,34);
    glVertex2f(-.08,.16);
    glVertex2f(-.082,.1);
    glVertex2f(.082,.1);
    glVertex2f(.08,.16);
    glEnd();

    //FLAG QUAD 1
    glBegin(GL_QUADS);
    glColor3ub(80,0,0);
    glVertex2f(-.06,.16);
    glVertex2f(-.06,.1);
    glVertex2f(.06,.1);
    glVertex2f(.06,.16);
    glEnd();

    //FLAG QUAD
    glBegin(GL_QUADS);
    glColor3ub(220,220,220);
    glVertex2f(-.08,.16);
    glVertex2f(-.082,.12);
    glVertex2f(-.06,.12);
    glVertex2f(-.06,.16);
    glEnd();

    //FLAG QUAD
    glBegin(GL_QUADS);
    glColor3ub(220,220,220);
    glVertex2f(.08,.16);
    glVertex2f(.082,.12);
    glVertex2f(.06,.12);
    glVertex2f(.06,.16);
    glEnd();





    //BD FLAG STAND
    glLineWidth(1);
    glBegin(GL_LINES);
    glColor3ub(238,232,170);
    glVertex2f(0,.16);
    glVertex2f(0,.3);
    glEnd();

    glBegin(GL_QUADS);
    glColor3ub(0,102,0);
    glVertex2f(0,.29);
    glVertex2f(0,.25);
    glVertex2f(.02,.24);
    glVertex2f(.025,.27);
    glEnd();


    //FLAG CIRCLE
     x=0.01f;  y=.265f;  radius =.007f;
     triangleAmount = 20;
	 twicePi = 2.0f * PI;

	 glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(204,0,0);
		glVertex2f(x, y);
		for(int i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            x + (radius * cos(i *  twicePi / triangleAmount)),
			    y + (radius * sin(i * twicePi / triangleAmount))
			);
		}
	 glEnd();

}


    //Light
    {



    //LIGHT Left
    glBegin(GL_QUADS);
    glColor3ub(20,20,20);
    glVertex2f(-.22,.23);
    glVertex2f(-.22,.13);
    glVertex2f(-.21,.13);
    glVertex2f(-.21,.23);
    glEnd();

    //LIGHT Left Top Two
    glBegin(GL_QUADS);
    glColor3ub(20,20,20);
    glVertex2f(-.22,.23);
    glVertex2f(-.21,.23);
    glVertex2f(-.18,.24);
    glVertex2f(-.2,.25);

    glVertex2f(-.21,.23);
    glVertex2f(-.22,.23);
    glVertex2f(-.26,.24);
    glVertex2f(-.23,.25);
    glEnd();


    //LIGHT Right
    glBegin(GL_QUADS);
    glColor3ub(20,20,20);
    glVertex2f(.22,.23);
    glVertex2f(.22,.13);
    glVertex2f(.21,.13);
    glVertex2f(.21,.23);
    glEnd();


    //LIGHT Right Top Two
    glBegin(GL_QUADS);
    glColor3ub(20,20,20);
    glVertex2f(.22,.23);
    glVertex2f(.21,.23);
    glVertex2f(.18,.24);
    glVertex2f(.2,.25);

    glVertex2f(.21,.23);
    glVertex2f(.22,.23);
    glVertex2f(.26,.24);
    glVertex2f(.23,.25);
    glEnd();


    //ON LIGHT Left Top Two
    glBegin(GL_QUADS);
    glColor3ub(211, 228, 86);

    glVertex2f(-.19,.23);
    glVertex2f(-.2,.24);
    glVertex2f(-.21,.13);
    glVertex2f(-.15,.13);


    glVertex2f(-.24,.23);
    glVertex2f(-.23,.24);
    glVertex2f(-.225,.13);
    glVertex2f(-.29,.13);
    glEnd();






 //ON LIGHT Right Top Two
    glBegin(GL_QUADS);
    glColor3ub(211, 228, 86);

    glVertex2f(.19,.23);
    glVertex2f(.2,.24);
    glVertex2f(.21,.13);
    glVertex2f(.15,.13);


    glVertex2f(.24,.23);
    glVertex2f(.23,.24);
    glVertex2f(.225,.13);
    glVertex2f(.29,.13);
    glEnd();

    }

    //Base
{
     //Upper
    glBegin(GL_QUADS);
    glColor3ub(37,37,37);
    glVertex2f(-1,.07);
    glVertex2f(-1,.02);
    glVertex2f(1,.02);
    glVertex2f(1,.07);
    glEnd();
    //Mid
    glBegin(GL_QUADS);
    glColor3ub(65,12,2);
    glVertex2f(-1,.02);
    glVertex2f(-1,-.09);
    glVertex2f(1,-.09);
    glVertex2f(1,.02);
    glEnd();

    //Lower
    glBegin(GL_QUADS);
    glColor3ub(14,81,104);
    glVertex2f(-1,-.09);
    glVertex2f(-1,-.6);
    glVertex2f(1,-.6);
    glVertex2f(1,-.09);
    glEnd();
}





//Fence
{
    //Fence-Left-1
    glPushMatrix();
    glScalef(.8,.7,0);
    glTranslatef(-.25,-.73,0);
    glLineWidth(3);
    glBegin(GL_LINES);
    glColor3ub(176, 176, 172);
    glVertex2f(-1.0f,-0.1f);
    glVertex2f(-0.6f,-0.1f);

    glVertex2f(-1.0f,-0.05f);
    glVertex2f(-0.6f,-0.05f);

    glVertex2f(-1.0f,0.0f);
    glVertex2f(-0.6f,0.0f);

    glVertex2f(-1.0f,0.05f);
    glVertex2f(-0.6f,0.05f);

    glVertex2f(-1.0f,0.1f);
    glVertex2f(-0.6f,0.1f);

    glVertex2f(-0.95f,0.13f);
    glVertex2f(-0.95f,-0.12f);

    glVertex2f(-0.9f,0.13f);
    glVertex2f(-0.9f,-0.12f);

    glVertex2f(-0.85f,0.13f);
    glVertex2f(-0.85f,-0.12f);

    glVertex2f(-0.8f,0.13f);
    glVertex2f(-0.8f,-0.12f);

    glVertex2f(-0.75f,0.13f);
    glVertex2f(-0.75f,-0.12f);

    glVertex2f(-0.7f,0.13f);
    glVertex2f(-0.7f,-0.12f);

    glVertex2f(-0.65f,0.13f);
    glVertex2f(-0.65f,-0.12f);

    glEnd();
    glPopMatrix();

    //Fence-Left-2
    glPushMatrix();
    glScalef(.8,.7,0);
    glTranslatef(.105,-.73,0);
    glLineWidth(3);
    glBegin(GL_LINES);
    glColor3ub(176, 176, 172);
    glVertex2f(-1.0f,-0.1f);
    glVertex2f(-0.6f,-0.1f);

    glVertex2f(-1.0f,-0.05f);
    glVertex2f(-0.6f,-0.05f);

    glVertex2f(-1.0f,0.0f);
    glVertex2f(-0.6f,0.0f);

    glVertex2f(-1.0f,0.05f);
    glVertex2f(-0.6f,0.05f);

    glVertex2f(-1.0f,0.1f);
    glVertex2f(-0.6f,0.1f);

    glVertex2f(-0.95f,0.13f);
    glVertex2f(-0.95f,-0.12f);

    glVertex2f(-0.9f,0.13f);
    glVertex2f(-0.9f,-0.12f);

    glVertex2f(-0.85f,0.13f);
    glVertex2f(-0.85f,-0.12f);

    glVertex2f(-0.8f,0.13f);
    glVertex2f(-0.8f,-0.12f);

    glVertex2f(-0.75f,0.13f);
    glVertex2f(-0.75f,-0.12f);

    glVertex2f(-0.7f,0.13f);
    glVertex2f(-0.7f,-0.12f);

    glVertex2f(-0.65f,0.13f);
    glVertex2f(-0.65f,-0.12f);

    glEnd();
    glPopMatrix();

    //Fence-Left-3
    glPushMatrix();
    glScalef(.8,.7,0);
    glTranslatef(.46,-.73,0);
    glLineWidth(3);
    glBegin(GL_LINES);
    glColor3ub(176, 176, 172);
    glVertex2f(-1.0f,-0.1f);
    glVertex2f(-0.6f,-0.1f);

    glVertex2f(-1.0f,-0.05f);
    glVertex2f(-0.6f,-0.05f);

    glVertex2f(-1.0f,0.0f);
    glVertex2f(-0.6f,0.0f);

    glVertex2f(-1.0f,0.05f);
    glVertex2f(-0.6f,0.05f);

    glVertex2f(-1.0f,0.1f);
    glVertex2f(-0.6f,0.1f);

    glVertex2f(-0.95f,0.13f);
    glVertex2f(-0.95f,-0.12f);

    glVertex2f(-0.9f,0.13f);
    glVertex2f(-0.9f,-0.12f);

    glVertex2f(-0.85f,0.13f);
    glVertex2f(-0.85f,-0.12f);

    glVertex2f(-0.8f,0.13f);
    glVertex2f(-0.8f,-0.12f);

    glVertex2f(-0.75f,0.13f);
    glVertex2f(-0.75f,-0.12f);

    glVertex2f(-0.7f,0.13f);
    glVertex2f(-0.7f,-0.12f);

    glVertex2f(-0.65f,0.13f);
    glVertex2f(-0.65f,-0.12f);

    glEnd();
    glPopMatrix();

    //Fence-Left-4
    glPushMatrix();
    glScalef(.8,.7,0);
    glTranslatef(.815,-.73,0);
    glLineWidth(3);
    glBegin(GL_LINES);
    glColor3f(176, 176, 172);
    glVertex2f(-1.0f,-0.1f);
    glVertex2f(-0.6f,-0.1f);

    glVertex2f(-1.0f,-0.05f);
    glVertex2f(-0.6f,-0.05f);

    glVertex2f(-1.0f,0.0f);
    glVertex2f(-0.6f,0.0f);

    glVertex2f(-1.0f,0.05f);
    glVertex2f(-0.6f,0.05f);

    glVertex2f(-1.0f,0.1f);
    glVertex2f(-0.6f,0.1f);

    glVertex2f(-0.95f,0.13f);
    glVertex2f(-0.95f,-0.12f);

    glVertex2f(-0.9f,0.13f);
    glVertex2f(-0.9f,-0.12f);

    glVertex2f(-0.85f,0.13f);
    glVertex2f(-0.85f,-0.12f);

    glVertex2f(-0.8f,0.13f);
    glVertex2f(-0.8f,-0.12f);

    glVertex2f(-0.75f,0.13f);
    glVertex2f(-0.75f,-0.12f);

    glVertex2f(-0.7f,0.13f);
    glVertex2f(-0.7f,-0.12f);

    glVertex2f(-0.65f,0.13f);
    glVertex2f(-0.65f,-0.12f);

    glEnd();
    glPopMatrix();

    //Fence-Left-5
    glPushMatrix();
    glScalef(.8,.7,0);
    glTranslatef(1.17,-.73,0);
    glLineWidth(3);
    glBegin(GL_LINES);
    glColor3ub(176, 176, 172);
    glVertex2f(-1.0f,-0.1f);
    glVertex2f(-0.6f,-0.1f);

    glVertex2f(-1.0f,-0.05f);
    glVertex2f(-0.6f,-0.05f);

    glVertex2f(-1.0f,0.0f);
    glVertex2f(-0.6f,0.0f);

    glVertex2f(-1.0f,0.05f);
    glVertex2f(-0.6f,0.05f);

    glVertex2f(-1.0f,0.1f);
    glVertex2f(-0.6f,0.1f);

    glVertex2f(-0.95f,0.13f);
    glVertex2f(-0.95f,-0.12f);

    glVertex2f(-0.9f,0.13f);
    glVertex2f(-0.9f,-0.12f);

    glVertex2f(-0.85f,0.13f);
    glVertex2f(-0.85f,-0.12f);

    glVertex2f(-0.8f,0.13f);
    glVertex2f(-0.8f,-0.12f);

    glVertex2f(-0.75f,0.13f);
    glVertex2f(-0.75f,-0.12f);

    glVertex2f(-0.7f,0.13f);
    glVertex2f(-0.7f,-0.12f);

    glVertex2f(-0.65f,0.13f);
    glVertex2f(-0.65f,-0.12f);

    glEnd();
    glPopMatrix();

    //Fence-Left-6
    glPushMatrix();
    glScalef(.8,.7,0);
    glTranslatef(1.525,-.73,0);
    glLineWidth(3);
    glBegin(GL_LINES);
    glColor3ub(176, 176, 172);
    glVertex2f(-1.0f,-0.1f);
    glVertex2f(-0.6f,-0.1f);

    glVertex2f(-1.0f,-0.05f);
    glVertex2f(-0.6f,-0.05f);

    glVertex2f(-1.0f,0.0f);
    glVertex2f(-0.6f,0.0f);

    glVertex2f(-1.0f,0.05f);
    glVertex2f(-0.6f,0.05f);

    glVertex2f(-1.0f,0.1f);
    glVertex2f(-0.6f,0.1f);

    glVertex2f(-0.95f,0.13f);
    glVertex2f(-0.95f,-0.12f);

    glVertex2f(-0.9f,0.13f);
    glVertex2f(-0.9f,-0.12f);

    glVertex2f(-0.85f,0.13f);
    glVertex2f(-0.85f,-0.12f);

    glVertex2f(-0.8f,0.13f);
    glVertex2f(-0.8f,-0.12f);

    glVertex2f(-0.75f,0.13f);
    glVertex2f(-0.75f,-0.12f);

    glVertex2f(-0.7f,0.13f);
    glVertex2f(-0.7f,-0.12f);

    glVertex2f(-0.65f,0.13f);
    glVertex2f(-0.65f,-0.12f);

    glEnd();
    glPopMatrix();

    //Fence-Left-7
    glPushMatrix();
    glScalef(.8,.7,0);
    glTranslatef(1.88,-.73,0);
    glLineWidth(3);
    glBegin(GL_LINES);
    glColor3ub(176, 176, 172);
    glVertex2f(-1.0f,-0.1f);
    glVertex2f(-0.6f,-0.1f);

    glVertex2f(-1.0f,-0.05f);
    glVertex2f(-0.6f,-0.05f);

    glVertex2f(-1.0f,0.0f);
    glVertex2f(-0.6f,0.0f);

    glVertex2f(-1.0f,0.05f);
    glVertex2f(-0.6f,0.05f);

    glVertex2f(-1.0f,0.1f);
    glVertex2f(-0.6f,0.1f);

    glVertex2f(-0.95f,0.13f);
    glVertex2f(-0.95f,-0.12f);

    glVertex2f(-0.9f,0.13f);
    glVertex2f(-0.9f,-0.12f);

    glVertex2f(-0.85f,0.13f);
    glVertex2f(-0.85f,-0.12f);

    glVertex2f(-0.8f,0.13f);
    glVertex2f(-0.8f,-0.12f);

    glVertex2f(-0.75f,0.13f);
    glVertex2f(-0.75f,-0.12f);

    glVertex2f(-0.7f,0.13f);
    glVertex2f(-0.7f,-0.12f);

    glVertex2f(-0.65f,0.13f);
    glVertex2f(-0.65f,-0.12f);

    glEnd();
    glPopMatrix();

}


    //Footpath
    {
    glBegin(GL_QUADS);
    glColor3ub(82, 80, 79);
    glVertex2f(-1,-.6);
    glVertex2f(-1,-.66);
    glVertex2f(1,-.66);
    glVertex2f(1,-.6);
    glEnd();

    glBegin(GL_QUADS);
    glColor3ub(176, 176, 172);
    glVertex2f(-1,-.66);
    glVertex2f(-1,-.67);
    glVertex2f(1,-.67);
    glVertex2f(1,-.66);
    glEnd();
    }
//Road / Car
{



    //Car-Below-Left
    glPushMatrix();
    glTranslatef(position2,0.0f,0.0f);
    glTranslatef(.11,-.29,0);
    glBegin(GL_POLYGON);
    glColor3ub(255,0,0);
    glVertex2f(-.66,-.60);
    glVertex2f(-.66,-.68);
    glVertex2f(-.28,-.68);
    glVertex2f(-.28,-.62);
    glVertex2f(-.27,-.62);
    glVertex2f(-.28,-.60);
    glVertex2f(-.36,-.60);
    glVertex2f(-.40,-.54);
    glVertex2f(-.60,-.54);
    glVertex2f(-.62,-.62);
    glEnd();

    glBegin(GL_QUADS);
    glColor3ub(255,255,255);
    glVertex2f(-.37,-.60);
    glVertex2f(-.40,-.55);
    glVertex2f(-.58,-.55);
    glVertex2f(-.62,-.60);
    glEnd();

    glBegin(GL_LINES);
    glColor3ub(0,0,0);

    glVertex2f(-.40,-.55);
    glVertex2f(-.40,-.60);

    glVertex2f(-.58,-.55);
    glVertex2f(-.58,-.60);
    glEnd();

//car wheel back
    int i;
    x=-.58f; y=-.68f; radius =.03f;
	triangleAmount = 20;
	twicePi = 2.0f * PI;

	glBegin(GL_TRIANGLE_FAN);
	glColor3ub(0,0,0);
    glVertex2f(x, y);
    for(i = 0; i <= triangleAmount;i++)
    {
        glVertex2f
        (
                x + (radius * cos(i *  twicePi / triangleAmount)),
			    y + (radius * sin(i * twicePi / triangleAmount))
        );
    }
	glEnd();
//-----------
	 x=-.58f;  y=-.68f;  radius =.018f;
    triangleAmount = 20;
    twicePi = 2.0f * PI;

	glBegin(GL_TRIANGLE_FAN);
	glColor3ub(255,250,250);
    glVertex2f(x, y);
    for(i = 0; i <= triangleAmount;i++)
    {
        glVertex2f
        (
                x + (radius * cos(i *  twicePi / triangleAmount)),
			    y + (radius * sin(i * twicePi / triangleAmount))
        );
    }
	glEnd();

//car wheel front
	x=-.34f;  y=-.68f;  radius =.03f;
    triangleAmount = 20;
    twicePi = 2.0f * PI;

	glBegin(GL_TRIANGLE_FAN);
	glColor3ub(0,0,0);
    glVertex2f(x, y);
    for(i = 0; i <= triangleAmount;i++)
    {
        glVertex2f
        (
                x + (radius * cos(i *  twicePi / triangleAmount)),
			    y + (radius * sin(i * twicePi / triangleAmount))
        );
    }
	glEnd();
//-----------------
	x=-.34f;  y=-.68f;  radius =.018f;
    triangleAmount = 20;
    twicePi = 2.0f * PI;

	glBegin(GL_TRIANGLE_FAN);
	glColor3ub(255,250,250);
    glVertex2f(x, y);
    for(i = 0; i <= triangleAmount;i++)
    {
        glVertex2f
        (
                x + (radius * cos(i *  twicePi / triangleAmount)),
			    y + (radius * sin(i * twicePi / triangleAmount))
        );
    }
	glEnd();
    glPopMatrix();


}

//Road side tree
{
    //Left-1
    glPushMatrix();
    glScalef(.5,.4,0);
    glTranslatef(-.9,-1.4,0);
    glBegin(GL_POLYGON);
    glColor3ub(102, 51, 0);
    glVertex2f(-0.72f,-0.15f);
    glVertex2f(-0.65f,-0.2f);
    glVertex2f(-0.735f,-0.17f);
    glVertex2f(-0.74f,-0.25f);
    glVertex2f(-0.775f,-0.17f);
    glVertex2f(-0.85f,-0.2f);
    glVertex2f(-0.78f,-0.15f);
    glEnd();

    glBegin(GL_QUADS);
    glColor3ub(102, 51, 0);
    glVertex2f(-0.78f,-0.15f);
    glVertex2f(-0.78f,0.23f);
    glVertex2f(-0.72f,0.23f);
    glVertex2f(-0.72f,-0.15f);
    glEnd();
    glBegin(GL_QUADS);
    glColor3ub(102, 51, 0);
    glVertex2f(-0.76f,0.23f);
    glVertex2f(-0.76f,0.3f);
    glVertex2f(-0.74f,0.3f);
    glVertex2f(-0.74f,0.23f);
    glEnd();
    glBegin(GL_QUADS);
    glColor3ub(102, 51, 0);
    glVertex2f(-0.74f,0.23f);
    glVertex2f(-0.71f,0.29f);
    glVertex2f(-0.7f,0.28f);
    glVertex2f(-0.72f,0.23f);
    glEnd();
    glBegin(GL_QUADS);
    glColor3ub(102, 51, 0);
    glVertex2f(-0.78f,0.23f);
    glVertex2f(-0.8f,0.28f);
    glVertex2f(-0.79f,0.29f);
    glVertex2f(-0.76f,0.23f);
    glEnd();

    int i;

	 x=-.75f;  y=.33f;  radius =.06f;
	triangleAmount = 20;
    twicePi = 2.0f * PI;

	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(60, 149, 76);
		glVertex2f(x, y);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            x + (radius * cos(i *  twicePi / triangleAmount)),
			    y + (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();

    GLfloat a=-.68f; GLfloat b=.31f;

	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(60, 149, 76);
		glVertex2f(a, b);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            a + (radius * cos(i *  twicePi / triangleAmount)),
			    b + (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();

	GLfloat c=-.81f; GLfloat d=.31f;

	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(60, 149, 76);
		glVertex2f(c, d);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            c + (radius * cos(i *  twicePi / triangleAmount)),
			    d + (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();

	GLfloat e=-.87f; GLfloat f=.35f;

	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(60, 149, 76);
		glVertex2f(e, f);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            e + (radius * cos(i *  twicePi / triangleAmount)),
			    f+ (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();

	GLfloat g=-.61f; GLfloat h=.35f;

	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(60, 149, 76);
		glVertex2f(g, h);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            g + (radius * cos(i *  twicePi / triangleAmount)),
			    h+ (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();
	GLfloat a1=-.61f; GLfloat b1=.4f;

	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(60, 149, 76);
		glVertex2f(a1, b1);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            a1 + (radius * cos(i *  twicePi / triangleAmount)),
			    b1 + (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();

	GLfloat c1=-.88f; GLfloat d1=.4f;

	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(60, 149, 76);
		glVertex2f(c, d);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            c1 + (radius * cos(i *  twicePi / triangleAmount)),
			    d1 + (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();

	GLfloat e1=-.87f; GLfloat f1=.44f;

	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(60, 149, 76);
		glVertex2f(e1, f1);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            e1 + (radius * cos(i *  twicePi / triangleAmount)),
			    f1+ (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();

	GLfloat g1=-.61f; GLfloat h1=.4f;

	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(60, 149, 76);
		glVertex2f(g, h);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            g1 + (radius * cos(i *  twicePi / triangleAmount)),
			    h1+ (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();

	GLfloat e11=-.64f; GLfloat f11=.44f;
	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(60, 149, 76);
		glVertex2f(e11, f11);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            e11 + (radius * cos(i *  twicePi / triangleAmount)),
			    f11+ (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();

	GLfloat e12=-.75f; GLfloat f12=.44f;
	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(60, 149, 76);
		glVertex2f(e12, f12);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            e12 + (radius * cos(i *  twicePi / triangleAmount)),
			    f12+ (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();

    glBegin(GL_QUADS);
    glColor3ub(60, 149, 76);
    glVertex2f(-0.85f,0.33f);
    glVertex2f(-0.85f,0.44f);
    glVertex2f(-0.65f,0.44f);
    glVertex2f(-0.65f,0.33f);
    glEnd();

    GLfloat e123=-.8f; GLfloat f123=.5f;
	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(60, 149, 76);
		glVertex2f(e123, f123);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            e123 + (radius * cos(i *  twicePi / triangleAmount)),
			    f123+ (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();
	GLfloat e1232=-.7f; GLfloat f1232=.5f;

	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(60, 149, 76);
		glVertex2f(e1232, f1232);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            e1232 + (radius * cos(i *  twicePi / triangleAmount)),
			    f1232+ (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();
	glPopMatrix();


	//Left-2
    glPushMatrix();
    glScalef(.5,.4,0);
    glTranslatef(.35,-1.4,0);
    glBegin(GL_POLYGON);
    glColor3ub(102, 51, 0);
    glVertex2f(-0.72f,-0.15f);
    glVertex2f(-0.65f,-0.2f);
    glVertex2f(-0.735f,-0.17f);
    glVertex2f(-0.74f,-0.25f);
    glVertex2f(-0.775f,-0.17f);
    glVertex2f(-0.85f,-0.2f);
    glVertex2f(-0.78f,-0.15f);
    glEnd();

    glBegin(GL_QUADS);
    glColor3ub(102, 51, 0);
    glVertex2f(-0.78f,-0.15f);
    glVertex2f(-0.78f,0.23f);
    glVertex2f(-0.72f,0.23f);
    glVertex2f(-0.72f,-0.15f);
    glEnd();
    glBegin(GL_QUADS);
    glColor3ub(102, 51, 0);
    glVertex2f(-0.76f,0.23f);
    glVertex2f(-0.76f,0.3f);
    glVertex2f(-0.74f,0.3f);
    glVertex2f(-0.74f,0.23f);
    glEnd();
    glBegin(GL_QUADS);
    glColor3ub(102, 51, 0);
    glVertex2f(-0.74f,0.23f);
    glVertex2f(-0.71f,0.29f);
    glVertex2f(-0.7f,0.28f);
    glVertex2f(-0.72f,0.23f);
    glEnd();
    glBegin(GL_QUADS);
    glColor3ub(102, 51, 0);
    glVertex2f(-0.78f,0.23f);
    glVertex2f(-0.8f,0.28f);
    glVertex2f(-0.79f,0.29f);
    glVertex2f(-0.76f,0.23f);
    glEnd();


	 x=-.75f;  y=.33f;  radius =.06f;
	triangleAmount = 20;
    twicePi = 2.0f * PI;

	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(60, 149, 76);
		glVertex2f(x, y);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            x + (radius * cos(i *  twicePi / triangleAmount)),
			    y + (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();

    a=-.68f;  b=.31f;

	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(60, 149, 76);
		glVertex2f(a, b);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            a + (radius * cos(i *  twicePi / triangleAmount)),
			    b + (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();

	 c=-.81f;  d=.31f;

	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(60, 149, 76);
		glVertex2f(c, d);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            c + (radius * cos(i *  twicePi / triangleAmount)),
			    d + (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();

	 e=-.87f;  f=.35f;

	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(60, 149, 76);
		glVertex2f(e, f);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            e + (radius * cos(i *  twicePi / triangleAmount)),
			    f+ (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();

	 g=-.61f;  h=.35f;

	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(60, 149, 76);
		glVertex2f(g, h);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            g + (radius * cos(i *  twicePi / triangleAmount)),
			    h+ (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();
	 a1=-.61f;  b1=.4f;

	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(60, 149, 76);
		glVertex2f(a1, b1);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            a1 + (radius * cos(i *  twicePi / triangleAmount)),
			    b1 + (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();

	 c1=-.88f;  d1=.4f;

	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(60, 149, 76);
		glVertex2f(c, d);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            c1 + (radius * cos(i *  twicePi / triangleAmount)),
			    d1 + (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();

	 e1=-.87f;  f1=.44f;

	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(60, 149, 76);
		glVertex2f(e1, f1);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            e1 + (radius * cos(i *  twicePi / triangleAmount)),
			    f1+ (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();

	 g1=-.61f;  h1=.4f;

	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(60, 149, 76);
		glVertex2f(g, h);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            g1 + (radius * cos(i *  twicePi / triangleAmount)),
			    h1+ (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();

	 e11=-.64f;  f11=.44f;
	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(60, 149, 76);
		glVertex2f(e11, f11);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            e11 + (radius * cos(i *  twicePi / triangleAmount)),
			    f11+ (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();

	 e12=-.75f;  f12=.44f;
	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(60, 149, 76);
		glVertex2f(e12, f12);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            e12 + (radius * cos(i *  twicePi / triangleAmount)),
			    f12+ (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();

    glBegin(GL_QUADS);
    glColor3ub(60, 149, 76);
    glVertex2f(-0.85f,0.33f);
    glVertex2f(-0.85f,0.44f);
    glVertex2f(-0.65f,0.44f);
    glVertex2f(-0.65f,0.33f);
    glEnd();

    e123=-.8f;  f123=.5f;
	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(60, 149, 76);
		glVertex2f(e123, f123);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            e123 + (radius * cos(i *  twicePi / triangleAmount)),
			    f123+ (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();
	 e1232=-.7f;  f1232=.5f;

	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(60, 149, 76);
		glVertex2f(e1232, f1232);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            e1232 + (radius * cos(i *  twicePi / triangleAmount)),
			    f1232+ (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();
	glPopMatrix();

	//Left-3
    glPushMatrix();
    glScalef(.5,.4,0);
    glTranslatef(1.6,-1.4,0);
    glBegin(GL_POLYGON);
    glColor3ub(102, 51, 0);
    glVertex2f(-0.72f,-0.15f);
    glVertex2f(-0.65f,-0.2f);
    glVertex2f(-0.735f,-0.17f);
    glVertex2f(-0.74f,-0.25f);
    glVertex2f(-0.775f,-0.17f);
    glVertex2f(-0.85f,-0.2f);
    glVertex2f(-0.78f,-0.15f);
    glEnd();

    glBegin(GL_QUADS);
    glColor3ub(102, 51, 0);
    glVertex2f(-0.78f,-0.15f);
    glVertex2f(-0.78f,0.23f);
    glVertex2f(-0.72f,0.23f);
    glVertex2f(-0.72f,-0.15f);
    glEnd();
    glBegin(GL_QUADS);
    glColor3ub(102, 51, 0);
    glVertex2f(-0.76f,0.23f);
    glVertex2f(-0.76f,0.3f);
    glVertex2f(-0.74f,0.3f);
    glVertex2f(-0.74f,0.23f);
    glEnd();
    glBegin(GL_QUADS);
    glColor3ub(102, 51, 0);
    glVertex2f(-0.74f,0.23f);
    glVertex2f(-0.71f,0.29f);
    glVertex2f(-0.7f,0.28f);
    glVertex2f(-0.72f,0.23f);
    glEnd();
    glBegin(GL_QUADS);
    glColor3ub(102, 51, 0);
    glVertex2f(-0.78f,0.23f);
    glVertex2f(-0.8f,0.28f);
    glVertex2f(-0.79f,0.29f);
    glVertex2f(-0.76f,0.23f);
    glEnd();


	 x=-.75f;  y=.33f;  radius =.06f;
	triangleAmount = 20;
    twicePi = 2.0f * PI;

	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(60, 149, 76);
		glVertex2f(x, y);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            x + (radius * cos(i *  twicePi / triangleAmount)),
			    y + (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();

    a=-.68f;  b=.31f;

	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(60, 149, 76);
		glVertex2f(a, b);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            a + (radius * cos(i *  twicePi / triangleAmount)),
			    b + (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();

	 c=-.81f;  d=.31f;

	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(60, 149, 76);
		glVertex2f(c, d);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            c + (radius * cos(i *  twicePi / triangleAmount)),
			    d + (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();

	 e=-.87f;  f=.35f;

	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(60, 149, 76);
		glVertex2f(e, f);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            e + (radius * cos(i *  twicePi / triangleAmount)),
			    f+ (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();

	 g=-.61f;  h=.35f;

	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(60, 149, 76);
		glVertex2f(g, h);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            g + (radius * cos(i *  twicePi / triangleAmount)),
			    h+ (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();
	 a1=-.61f;  b1=.4f;

	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(60, 149, 76);
		glVertex2f(a1, b1);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            a1 + (radius * cos(i *  twicePi / triangleAmount)),
			    b1 + (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();

	 c1=-.88f;  d1=.4f;

	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(60, 149, 76);
		glVertex2f(c, d);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            c1 + (radius * cos(i *  twicePi / triangleAmount)),
			    d1 + (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();

	 e1=-.87f;  f1=.44f;

	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(60, 149, 76);
		glVertex2f(e1, f1);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            e1 + (radius * cos(i *  twicePi / triangleAmount)),
			    f1+ (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();

	 g1=-.61f;  h1=.4f;

	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(60, 149, 76);
		glVertex2f(g, h);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            g1 + (radius * cos(i *  twicePi / triangleAmount)),
			    h1+ (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();

	 e11=-.64f;  f11=.44f;
	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(60, 149, 76);
		glVertex2f(e11, f11);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            e11 + (radius * cos(i *  twicePi / triangleAmount)),
			    f11+ (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();

	 e12=-.75f;  f12=.44f;
	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(60, 149, 76);
		glVertex2f(e12, f12);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            e12 + (radius * cos(i *  twicePi / triangleAmount)),
			    f12+ (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();

    glBegin(GL_QUADS);
    glColor3ub(60, 149, 76);
    glVertex2f(-0.85f,0.33f);
    glVertex2f(-0.85f,0.44f);
    glVertex2f(-0.65f,0.44f);
    glVertex2f(-0.65f,0.33f);
    glEnd();

    e123=-.8f;  f123=.5f;
	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(60, 149, 76);
		glVertex2f(e123, f123);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            e123 + (radius * cos(i *  twicePi / triangleAmount)),
			    f123+ (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();
	 e1232=-.7f;  f1232=.5f;

	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(60, 149, 76);
		glVertex2f(e1232, f1232);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            e1232 + (radius * cos(i *  twicePi / triangleAmount)),
			    f1232+ (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();
	glPopMatrix();

	//Left-4
    glPushMatrix();
    glScalef(.5,.4,0);
    glTranslatef(2.5,-1.4,0);
    glBegin(GL_POLYGON);
    glColor3ub(102, 51, 0);
    glVertex2f(-0.72f,-0.15f);
    glVertex2f(-0.65f,-0.2f);
    glVertex2f(-0.735f,-0.17f);
    glVertex2f(-0.74f,-0.25f);
    glVertex2f(-0.775f,-0.17f);
    glVertex2f(-0.85f,-0.2f);
    glVertex2f(-0.78f,-0.15f);
    glEnd();

    glBegin(GL_QUADS);
    glColor3ub(102, 51, 0);
    glVertex2f(-0.78f,-0.15f);
    glVertex2f(-0.78f,0.23f);
    glVertex2f(-0.72f,0.23f);
    glVertex2f(-0.72f,-0.15f);
    glEnd();
    glBegin(GL_QUADS);
    glColor3ub(102, 51, 0);
    glVertex2f(-0.76f,0.23f);
    glVertex2f(-0.76f,0.3f);
    glVertex2f(-0.74f,0.3f);
    glVertex2f(-0.74f,0.23f);
    glEnd();
    glBegin(GL_QUADS);
    glColor3ub(102, 51, 0);
    glVertex2f(-0.74f,0.23f);
    glVertex2f(-0.71f,0.29f);
    glVertex2f(-0.7f,0.28f);
    glVertex2f(-0.72f,0.23f);
    glEnd();
    glBegin(GL_QUADS);
    glColor3ub(102, 51, 0);
    glVertex2f(-0.78f,0.23f);
    glVertex2f(-0.8f,0.28f);
    glVertex2f(-0.79f,0.29f);
    glVertex2f(-0.76f,0.23f);
    glEnd();


	 x=-.75f;  y=.33f;  radius =.06f;
	triangleAmount = 20;
    twicePi = 2.0f * PI;

	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(60, 149, 76);
		glVertex2f(x, y);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            x + (radius * cos(i *  twicePi / triangleAmount)),
			    y + (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();

    a=-.68f;  b=.31f;

	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(60, 149, 76);
		glVertex2f(a, b);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            a + (radius * cos(i *  twicePi / triangleAmount)),
			    b + (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();

	 c=-.81f;  d=.31f;

	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(60, 149, 76);
		glVertex2f(c, d);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            c + (radius * cos(i *  twicePi / triangleAmount)),
			    d + (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();

	 e=-.87f;  f=.35f;

	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(60, 149, 76);
		glVertex2f(e, f);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            e + (radius * cos(i *  twicePi / triangleAmount)),
			    f+ (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();

	 g=-.61f;  h=.35f;

	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(60, 149, 76);
		glVertex2f(g, h);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            g + (radius * cos(i *  twicePi / triangleAmount)),
			    h+ (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();
	 a1=-.61f;  b1=.4f;

	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(60, 149, 76);
		glVertex2f(a1, b1);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            a1 + (radius * cos(i *  twicePi / triangleAmount)),
			    b1 + (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();

	 c1=-.88f;  d1=.4f;

	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(60, 149, 76);
		glVertex2f(c, d);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            c1 + (radius * cos(i *  twicePi / triangleAmount)),
			    d1 + (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();

	 e1=-.87f;  f1=.44f;

	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(60, 149, 76);
		glVertex2f(e1, f1);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            e1 + (radius * cos(i *  twicePi / triangleAmount)),
			    f1+ (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();

	 g1=-.61f;  h1=.4f;

	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(60, 149, 76);
		glVertex2f(g, h);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            g1 + (radius * cos(i *  twicePi / triangleAmount)),
			    h1+ (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();

	 e11=-.64f;  f11=.44f;
	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(60, 149, 76);
		glVertex2f(e11, f11);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            e11 + (radius * cos(i *  twicePi / triangleAmount)),
			    f11+ (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();

	 e12=-.75f;  f12=.44f;
	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(60, 149, 76);
		glVertex2f(e12, f12);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            e12 + (radius * cos(i *  twicePi / triangleAmount)),
			    f12+ (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();

    glBegin(GL_QUADS);
    glColor3ub(60, 149, 76);
    glVertex2f(-0.85f,0.33f);
    glVertex2f(-0.85f,0.44f);
    glVertex2f(-0.65f,0.44f);
    glVertex2f(-0.65f,0.33f);
    glEnd();

    e123=-.8f;  f123=.5f;
	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(60, 149, 76);
		glVertex2f(e123, f123);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            e123 + (radius * cos(i *  twicePi / triangleAmount)),
			    f123+ (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();
	 e1232=-.7f;  f1232=.5f;

	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(60, 149, 76);
		glVertex2f(e1232, f1232);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            e1232 + (radius * cos(i *  twicePi / triangleAmount)),
			    f1232+ (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();
	glPopMatrix();

}


//Light
{


//LIGHT Left
    glPushMatrix();
    glTranslatef(-.3,-.65,0);

    glBegin(GL_QUADS);
    glColor3ub(20,20,20);
    glVertex2f(-.22,.23);
    glVertex2f(-.22,.02);
    glVertex2f(-.21,.02);
    glVertex2f(-.21,.23);
    glEnd();


    //LIGHT Left Top Two
    glBegin(GL_QUADS);
    glColor3ub(20,20,20);
    glVertex2f(-.22,.23);
    glVertex2f(-.21,.23);
    glVertex2f(-.18,.24);
    glVertex2f(-.2,.25);

    glVertex2f(-.21,.23);
    glVertex2f(-.22,.23);
    glVertex2f(-.26,.24);
    glVertex2f(-.23,.25);
    glEnd();
    glLoadIdentity();
    glPopMatrix();


    //LIGHT Right
    glPushMatrix();
    glTranslatef(0,-.65,0);
    glBegin(GL_QUADS);
    glColor3ub(20,20,20);
    glVertex2f(.22,.23);
    glVertex2f(.22,.02);
    glVertex2f(.21,.02);
    glVertex2f(.21,.23);
    glEnd();


    //LIGHT Right Top Two

    glBegin(GL_QUADS);
    glColor3ub(20,20,20);
    glVertex2f(.22,.23);
    glVertex2f(.21,.23);
    glVertex2f(.18,.24);
    glVertex2f(.2,.25);

    glVertex2f(.21,.23);
    glVertex2f(.22,.23);
    glVertex2f(.26,.24);
    glVertex2f(.23,.25);
    glEnd();
    glLoadIdentity();
    glPopMatrix();


    //ON LIGHT Left Top Two
    glPushMatrix();

    glTranslatef(-.3,-.65,0);
    glBegin(GL_QUADS);
    glColor3ub(211, 228, 86);

    glVertex2f(-.19,.23);
    glVertex2f(-.2,.24);
    glVertex2f(-.2,.02);
    glVertex2f(-.07,.02);


    glVertex2f(-.24,.23);
    glVertex2f(-.23,.24);
    glVertex2f(-.225,.02);
    glVertex2f(-.35,.02);
    glEnd();
    glLoadIdentity();
    glPopMatrix();






 //ON LIGHT Right Top Two
    glPushMatrix();
    glTranslatef(0,-.65,0);
    glBegin(GL_QUADS);
    glColor3ub(211, 228, 86);

    glVertex2f(.19,.23);
    glVertex2f(.2,.24);
    glVertex2f(.21,.02);
    glVertex2f(.07,.02);


    glVertex2f(.24,.23);
    glVertex2f(.23,.24);
    glVertex2f(.225,.02);
    glVertex2f(.35,.02);
    glEnd();
    glLoadIdentity();
    glPopMatrix();





//LIGHT Left
    glPushMatrix();
    glTranslatef(-.75,-.65,0);

    glBegin(GL_QUADS);
    glColor3ub(20,20,20);
    glVertex2f(-.22,.23);
    glVertex2f(-.22,.02);
    glVertex2f(-.21,.02);
    glVertex2f(-.21,.23);
    glEnd();


    //LIGHT Left Top Two
    glBegin(GL_QUADS);
    glColor3ub(20,20,20);
    glVertex2f(-.22,.23);
    glVertex2f(-.21,.23);
    glVertex2f(-.18,.24);
    glVertex2f(-.2,.25);

    glVertex2f(-.21,.23);
    glVertex2f(-.22,.23);
    glVertex2f(-.26,.24);
    glVertex2f(-.23,.25);
    glEnd();
    glLoadIdentity();
    glPopMatrix();


    //LIGHT Right
    glPushMatrix();
    glTranslatef(.5,-.65,0);
    glBegin(GL_QUADS);
    glColor3ub(20,20,20);
    glVertex2f(.22,.23);
    glVertex2f(.22,.02);
    glVertex2f(.21,.02);
    glVertex2f(.21,.23);
    glEnd();


    //LIGHT Right Top Two

    glBegin(GL_QUADS);
    glColor3ub(20,20,20);
    glVertex2f(.22,.23);
    glVertex2f(.21,.23);
    glVertex2f(.18,.24);
    glVertex2f(.2,.25);

    glVertex2f(.21,.23);
    glVertex2f(.22,.23);
    glVertex2f(.26,.24);
    glVertex2f(.23,.25);
    glEnd();
    glLoadIdentity();
    glPopMatrix();


    //ON LIGHT Left Top Two
    glPushMatrix();

    glTranslatef(-.75,-.65,0);
    glBegin(GL_QUADS);
    glColor3ub(211, 228, 86);

    glVertex2f(-.19,.23);
    glVertex2f(-.2,.24);
    glVertex2f(-.2,.02);
    glVertex2f(-.07,.02);


    glVertex2f(-.24,.23);
    glVertex2f(-.23,.24);
    glVertex2f(-.225,.02);
    glVertex2f(-.35,.02);
    glEnd();
    glLoadIdentity();
    glPopMatrix();






 //ON LIGHT Right Top Two
    glPushMatrix();
    glTranslatef(.5,-.65,0);
    glBegin(GL_QUADS);
    glColor3ub(211, 228, 86);

    glVertex2f(.19,.23);
    glVertex2f(.2,.24);
    glVertex2f(.21,.02);
    glVertex2f(.07,.02);


    glVertex2f(.24,.23);
    glVertex2f(.23,.24);
    glVertex2f(.225,.02);
    glVertex2f(.35,.02);
    glEnd();
    glLoadIdentity();
    glPopMatrix();

}
 //Upper Car
 {


    glPushMatrix();
    glTranslatef(position,0.0f,0.0f);
    glTranslatef(0,-.38,0);
    glBegin(GL_POLYGON);
    glColor3ub(128,0,0);
    glVertex2f(.04,-.24);
    glVertex2f(0.0,-.34);
    glVertex2f(0,-.40);
    glVertex2f(.4,-.40);
    glVertex2f(.4,-.24);
    glEnd();

    glBegin(GL_QUADS);
    glColor3ub(240,255,240);
    glVertex2f(.37,-.26);
    glVertex2f(.30,-.26);
    glVertex2f(.30,-.34);
    glVertex2f(.37,-.34);
    glEnd();

    glBegin(GL_QUADS);
    glColor3ub(240,255,240);
    glVertex2f(.28,-.26);
    glVertex2f(.22,-.26);
    glVertex2f(.22,-.34);
    glVertex2f(.28,-.34);
    glEnd();

    glBegin(GL_QUADS);
    glColor3ub(240,255,240);
    glVertex2f(.20,-.26);
    glVertex2f(.14,-.26);
    glVertex2f(.14,-.34);
    glVertex2f(.20,-.34);
    glEnd();

    glBegin(GL_QUADS);
    glColor3ub(240,255,240);
    glVertex2f(.12,-.26);
    glVertex2f(.05,-.26);
    glVertex2f(.02,-.34);
    glVertex2f(.12,-.34);
    glEnd();
//car wheel front
	x=.08f;  y=-.40f;  radius =.04f;
    triangleAmount = 20;
    twicePi = 2.0f * PI;

	glBegin(GL_TRIANGLE_FAN);
	glColor3ub(0,0,0);
    glVertex2f(x, y);
    for(int i = 0; i <= triangleAmount;i++)
    {
        glVertex2f
        (
                x + (radius * cos(i *  twicePi / triangleAmount)),
			    y + (radius * sin(i * twicePi / triangleAmount))
        );
    }
	glEnd();
//-----------------
	x=.08f;  y=-.40f;  radius =.025f;
    triangleAmount = 20;
    twicePi = 2.0f * PI;

	glBegin(GL_TRIANGLE_FAN);
	glColor3ub(255,250,250);
    glVertex2f(x, y);
    for(int i = 0; i <= triangleAmount;i++)
    {
        glVertex2f
        (
                x + (radius * cos(i *  twicePi / triangleAmount)),
			    y + (radius * sin(i * twicePi / triangleAmount))
        );
    }
	glEnd();
//car wheel back
	x=.3f;  y=-.40f;  radius =.04f;
    triangleAmount = 20;
    twicePi = 2.0f * PI;

	glBegin(GL_TRIANGLE_FAN);
	glColor3ub(0,0,0);
    glVertex2f(x, y);
    for(int i = 0; i <= triangleAmount;i++)
    {
        glVertex2f
        (
                x + (radius * cos(i *  twicePi / triangleAmount)),
			    y + (radius * sin(i * twicePi / triangleAmount))
        );
    }
	glEnd();
//-----------------
	x=.3f;  y=-.40f;  radius =.025f;
    triangleAmount = 20;
    twicePi = 2.0f * PI;

	glBegin(GL_TRIANGLE_FAN);
	glColor3ub(255,250,250);
    glVertex2f(x, y);
    for(int i = 0; i <= triangleAmount;i++)
    {
        glVertex2f
        (
                x + (radius * cos(i *  twicePi / triangleAmount)),
			    y + (radius * sin(i * twicePi / triangleAmount))
        );
    }
	glEnd();
 }
    glPopMatrix();


   //glutTimerFunc(8000,rainy,0);

	glFlush();

}
}

void night(int value)
{
    glutDisplayFunc(nightView);
}


void day()
{

    glClearColor(1,1,1,1);
	glClear(GL_COLOR_BUFFER_BIT);
    speed=.1f;

    float x,  y,  radius,triangleAmount,twicePi;

//SKY / SUN / CLOUD
{



    //SKY
    glBegin(GL_QUADS);
    glColor3ub(255,255,255);
    glVertex2f(-1,1);
    glVertex2f(-1,.03);
    glVertex2f(1,.03);
    glVertex2f(1,1);
    glEnd();
    //first base
    glBegin(GL_QUADS);
    glColor3ub(255,178,102);
    glVertex2f(-1,1);
    glVertex2f(-1,.05);
    glVertex2f(1,.05);
    glVertex2f(1,1);
    glEnd();
   //sky
    glBegin(GL_QUADS);
    glColor3ub(73, 212, 240);
    glVertex2f(-1,1);
    glVertex2f(-1,.14);
    glVertex2f(1,.14);
    glVertex2f(1,1);
    glEnd();




    //Sun
    {



      //1st round effect
    {
        int i;
	GLfloat x=-.2f; GLfloat y=.91f; GLfloat radius =.26f;
	int triangleAmount = 20;
	GLfloat twicePi = 2.0f * PI;

	glBegin(GL_TRIANGLE_FAN);
    glColor3ub(99, 224, 249);
    glVertex2f(x, y);
    for(i = 0; i <= triangleAmount;i++){
        glVertex2f(
            x + (radius * cos(i *  twicePi / triangleAmount)),
            y + (radius * sin(i * twicePi / triangleAmount))
        );
    }
	glEnd();
    }

         //2nd round effect
    {
        int i;
	GLfloat x=-.2f; GLfloat y=.91f; GLfloat radius =.19f;
	int triangleAmount = 20;
	GLfloat twicePi = 2.0f * PI;

	glBegin(GL_TRIANGLE_FAN);
    glColor3ub(116, 227, 249);
    glVertex2f(x, y);
    for(i = 0; i <= triangleAmount;i++){
        glVertex2f(
            x + (radius * cos(i *  twicePi / triangleAmount)),
            y + (radius * sin(i * twicePi / triangleAmount))
        );
    }
	glEnd();
    }


        //3rd round effect
    {
        int i;
	GLfloat x=-.2f; GLfloat y=.91f; GLfloat radius =.13f;
	int triangleAmount = 20;
	GLfloat twicePi = 2.0f * PI;

	glBegin(GL_TRIANGLE_FAN);
    glColor3ub(143, 232, 250);
    glVertex2f(x, y);
    for(i = 0; i <= triangleAmount;i++){
        glVertex2f(
            x + (radius * cos(i *  twicePi / triangleAmount)),
            y + (radius * sin(i * twicePi / triangleAmount))
        );
    }
	glEnd();
    }


    //main
    {


    int i;
	GLfloat x=-.2f; GLfloat y=.91f; GLfloat radius =.07f;
	int triangleAmount = 20;
	GLfloat twicePi = 2.0f * PI;

	glBegin(GL_TRIANGLE_FAN);
    glColor3ub(255, 253, 200);
    glVertex2f(x, y);
    for(i = 0; i <= triangleAmount;i++){
        glVertex2f(
            x + (radius * cos(i *  twicePi / triangleAmount)),
            y + (radius * sin(i * twicePi / triangleAmount))
        );
    }
	glEnd();

    }
    }


    //Cloud
    {


    //upper cloud


    glPushMatrix();
    glTranslatef(.98,0.07f, 0.0f);
    x=-.24f; y=.74f; radius =.08f;
    triangleAmount = 20;
    twicePi = 2.0f * PI;

	glBegin(GL_TRIANGLE_FAN);
	glColor3ub(211,211,211);
    glVertex2f(x, y);
    int i;
    for(i = 0; i <= triangleAmount;i++)
    {
        glVertex2f
        (
            x + (radius * cos(i *  twicePi / triangleAmount)),
            y + (radius * sin(i * twicePi / triangleAmount))
        );
    }
	glEnd();

	x=-0.36f;  y=.78f;  radius =.08f;
    triangleAmount = 20;
    twicePi = 2.0f * PI;

	glBegin(GL_TRIANGLE_FAN);
	glColor3ub(211,211,211);
    glVertex2f(x, y);
    for(i = 0; i <= triangleAmount;i++)
    {
        glVertex2f
        (
            x + (radius * cos(i *  twicePi / triangleAmount)),
            y + (radius * sin(i * twicePi / triangleAmount))
        );
    }
	glEnd();

	x=-.47f;  y=.82f;  radius =.08f;
    triangleAmount = 20;
    twicePi = 2.0f * PI;

	glBegin(GL_TRIANGLE_FAN);
	glColor3ub(211,211,211);
    glVertex2f(x, y);
    for(i = 0; i <= triangleAmount;i++)
    {
        glVertex2f
        (
                x + (radius * cos(i *  twicePi / triangleAmount)),
			    y + (radius * sin(i * twicePi / triangleAmount))
        );
    }
	glEnd();



    //lower cloud
    x=-.33f;  y=.67f;  radius =.08f;
    triangleAmount = 20;
    twicePi = 2.0f * PI;

	glBegin(GL_TRIANGLE_FAN);
	glColor3ub(220,220,220);
    glVertex2f(x, y);
    for(i = 0; i <= triangleAmount;i++)
    {
        glVertex2f
        (
                x + (radius * cos(i *  twicePi / triangleAmount)),
			    y + (radius * sin(i * twicePi / triangleAmount))
        );
    }
	glEnd();

    x=-.44f;  y=.7f;  radius =.08f;
    triangleAmount = 20;
    twicePi = 2.0f * PI;

	glBegin(GL_TRIANGLE_FAN);
	glColor3ub(220,220,220);
    glVertex2f(x, y);
    for(i = 0; i <= triangleAmount;i++)
    {
        glVertex2f
        (
                x + (radius * cos(i *  twicePi / triangleAmount)),
			    y + (radius * sin(i * twicePi / triangleAmount))
        );
    }
	glEnd();

    x=-.54f;  y=.74f;  radius =.08f;
    triangleAmount = 20;
    twicePi = 2.0f * PI;

	glBegin(GL_TRIANGLE_FAN);
	glColor3ub(220,220,220);
    glVertex2f(x, y);
    for(i = 0; i <= triangleAmount;i++)
    {
        glVertex2f
        (
                x + (radius * cos(i *  twicePi / triangleAmount)),
			    y + (radius * sin(i * twicePi / triangleAmount))
        );
    }
	glEnd();

	x=-.6f;  y=.68f;  radius =.08f;
    triangleAmount = 20;
    twicePi = 2.0f * PI;

	glBegin(GL_TRIANGLE_FAN);
	glColor3ub(220,220,220);
    glVertex2f(x, y);
    for(i = 0; i <= triangleAmount;i++)
    {
        glVertex2f
        (
                x + (radius * cos(i *  twicePi / triangleAmount)),
			    y + (radius * sin(i * twicePi / triangleAmount))
        );
    }
	glEnd();

	x=-.49f;  y=.66f;  radius =.07f;
    triangleAmount = 20;
    twicePi = 2.0f * PI;

	glBegin(GL_TRIANGLE_FAN);
	glColor3ub(220,220,220);
    glVertex2f(x, y);
    for(i = 0; i <= triangleAmount;i++)
    {
        glVertex2f
        (
                x + (radius * cos(i *  twicePi / triangleAmount)),
			    y + (radius * sin(i * twicePi / triangleAmount))
        );
    }
	glEnd();
    }
	glPopMatrix();

}


//Mountain
{

       //building one
    glBegin(GL_QUADS);
    glColor3ub(146, 43, 33);
    glVertex2f(-0.6f, .6f);
    glVertex2f(-0.9f, .6f);
    glVertex2f(-.9f,.14f);
    glVertex2f(-0.6f,.14f);
    glEnd();

    glBegin(GL_QUADS); //first window
    glColor3ub(236, 240, 241);
    glVertex2f(-0.85f, .25f);
    glVertex2f(-0.89f, .25f);
    glVertex2f(-0.89f,.2f);
    glVertex2f(-0.85f,.2f);
    glEnd();

    glBegin(GL_QUADS);
    glColor3ub(236, 240, 241);
    glVertex2f(-0.77f, .25f);
    glVertex2f(-0.81f, .25f);
    glVertex2f(-0.81f,.2f);
    glVertex2f(-0.77f,.2f);
    glEnd();

    glBegin(GL_QUADS);
    glColor3ub(236, 240, 241);
    glVertex2f(-0.7f, .25f);
    glVertex2f(-0.74f, .25f);
    glVertex2f(-0.74f,.2f);
    glVertex2f(-0.7f,.2f);
    glEnd();

       glBegin(GL_QUADS);
    glColor3ub(236, 240, 241);
    glVertex2f(-0.62f, .25f);
    glVertex2f(-0.66f, .25f);
    glVertex2f(-0.66f,.2f);
    glVertex2f(-0.62f,.2f);
    glEnd();


     glBegin(GL_QUADS); //second window
    glColor3ub(236, 240, 241);
    glVertex2f(-0.85f, .35f);
    glVertex2f(-0.89f, .35f);
    glVertex2f(-0.89f,.3f);
    glVertex2f(-0.85f,.3f);
    glEnd();

    glBegin(GL_QUADS);
    glColor3ub(236, 240, 241);
    glVertex2f(-0.77f, .35f);
    glVertex2f(-0.81f, .35f);
    glVertex2f(-0.81f,.3f);
    glVertex2f(-0.77f,.3f);
    glEnd();

      glBegin(GL_QUADS);
    glColor3ub(236, 240, 241);
    glVertex2f(-0.7f, .35f);
    glVertex2f(-0.74f, .35f);
    glVertex2f(-0.74f,.3f);
    glVertex2f(-0.7f,.3f);
    glEnd();

     glBegin(GL_QUADS);
    glColor3ub(236, 240, 241);
    glVertex2f(-0.62f, .35f);
    glVertex2f(-0.66f, .35f);
    glVertex2f(-0.66f,.3f);
    glVertex2f(-0.62f,.3f);
    glEnd();

    glBegin(GL_QUADS); //third window
    glColor3ub(236, 240, 241);
    glVertex2f(-0.85f, .45f);
    glVertex2f(-0.89f, .45f);
    glVertex2f(-0.89f,.4f);
    glVertex2f(-0.85f,.4f);
    glEnd();

    glBegin(GL_QUADS);
    glColor3ub(236, 240, 241);
    glVertex2f(-0.77f, .45f);
    glVertex2f(-0.81f, .45f);
    glVertex2f(-0.81f,.4f);
    glVertex2f(-0.77f,.4f);
    glEnd();

      glBegin(GL_QUADS);
    glColor3ub(236, 240, 241);
    glVertex2f(-0.7f, .45f);
    glVertex2f(-0.74f, .45f);
    glVertex2f(-0.74f,.4f);
    glVertex2f(-0.7f,.4f);
    glEnd();

     glBegin(GL_QUADS);
    glColor3ub(236, 240, 241);
    glVertex2f(-0.62f, .45f);
    glVertex2f(-0.66f, .45f);
    glVertex2f(-0.66f,.4f);
    glVertex2f(-0.62f,.4f);
    glEnd();

     glBegin(GL_QUADS); //fourth window
    glColor3ub(236, 240, 241);
    glVertex2f(-0.85f, .55f);
    glVertex2f(-0.89f, .55f);
    glVertex2f(-0.89f,.5f);
    glVertex2f(-0.85f,.5f);
    glEnd();

    glBegin(GL_QUADS);
    glColor3ub(236, 240, 241);
    glVertex2f(-0.77f, .55f);
    glVertex2f(-0.81f, .55f);
    glVertex2f(-0.81f,.5f);
    glVertex2f(-0.77f,.5f);
    glEnd();

      glBegin(GL_QUADS);
    glColor3ub(236, 240, 241);
    glVertex2f(-0.7f, .55f);
    glVertex2f(-0.74f, .55f);
    glVertex2f(-0.74f,.5f);
    glVertex2f(-0.7f,.5f);
    glEnd();

     glBegin(GL_QUADS);
    glColor3ub(236, 240, 241);
    glVertex2f(-0.62f, .55f);
    glVertex2f(-0.66f, .55f);
    glVertex2f(-0.66f,.5f);
    glVertex2f(-0.62f,.5f);
    glEnd();

    //building two
     glBegin(GL_QUADS);
    glColor3ub(33, 97, 140 );
    glVertex2f(-0.25f, .84f);
    glVertex2f(-0.5f, .84f);
    glVertex2f(-.5f,.14f);
    glVertex2f(-0.25f,.14f);
    glEnd();

      glBegin(GL_LINES);
    glColor3ub(251, 252, 252 );
    glVertex2f(-0.5f, .24f);
    glVertex2f(-0.25f, .24f);
    glEnd();


      glBegin(GL_LINES);
    glColor3ub(251, 252, 252 );
    glVertex2f(-0.5f, .34f);
    glVertex2f(-0.25f, .34f);
    glEnd();


      glBegin(GL_LINES);
    glColor3ub(251, 252, 252 );
    glVertex2f(-0.5f, .44f);
    glVertex2f(-0.25f, .44f);
    glEnd();

       glBegin(GL_LINES);
    glColor3ub(251, 252, 252 );
    glVertex2f(-0.5f, .54f);
    glVertex2f(-0.25f, .54f);
    glEnd();

     glBegin(GL_LINES);
    glColor3ub(251, 252, 252 );
    glVertex2f(-0.5f, .64f);
    glVertex2f(-0.25f, .64f);
    glEnd();

     glBegin(GL_LINES);
    glColor3ub(251, 252, 252 );
    glVertex2f(-0.5f, .74f);
    glVertex2f(-0.25f, .74f);
    glEnd();

  //third building
    glBegin(GL_QUADS);
    glColor3ub(186, 74, 0 );
    glVertex2f(0.3f, .8f);
    glVertex2f(-0.2f, .8f);
    glVertex2f(-0.2f,.14f);
    glVertex2f(0.3f,.14f);
    glEnd();

    //door
    glBegin(GL_QUADS);
    glColor3ub(251, 252, 252);
    glVertex2f(0.1f, .3f);
    glVertex2f(0.01f, .3f);
    glVertex2f(0.01f,.14f);
    glVertex2f(0.1f,.14f);
    glEnd();

    // left windows
    glBegin(GL_QUADS);
    glColor3ub(251, 252, 252);
    glVertex2f(-0.01f, .3f);
    glVertex2f(-0.18f, .3f);
    glVertex2f(-0.18f,.2f);
    glVertex2f(-0.01f,.2f);
    glEnd();

     glBegin(GL_QUADS);
    glColor3ub(251, 252, 252);
    glVertex2f(-0.01f, .5f);
    glVertex2f(-0.18f, .5f);
    glVertex2f(-0.18f,.4f);
    glVertex2f(-0.01f,.4f);
    glEnd();

      glBegin(GL_QUADS);
    glColor3ub(251, 252, 252);
    glVertex2f(-0.01f, .7f);
    glVertex2f(-0.18f, .7f);
    glVertex2f(-0.18f,.6f);
    glVertex2f(-0.01f,.6f);
    glEnd();

    //right window

     glBegin(GL_QUADS);
    glColor3ub(251, 252, 252);
    glVertex2f(0.28f, .3f);
    glVertex2f(0.12f, .3f);
    glVertex2f(0.12f,.2f);
    glVertex2f(0.28f,.2f);
    glEnd();

      glBegin(GL_QUADS);
    glColor3ub(251, 252, 252);
    glVertex2f(0.28f, .5f);
    glVertex2f(0.12f, .5f);
    glVertex2f(0.12f,.4f);
    glVertex2f(0.28f,.4f);
    glEnd();

     glBegin(GL_QUADS);
    glColor3ub(251, 252, 252);
    glVertex2f(0.28f, .7f);
    glVertex2f(0.12f, .7f);
    glVertex2f(0.12f,.6f);
    glVertex2f(0.28f,.6f);
    glEnd();



   //fourth building
    glBegin(GL_QUADS);
    glColor3ub(125, 102, 8  );
    glVertex2f(0.7f, .6f);
    glVertex2f(0.35f, .6f);
    glVertex2f(0.35f,.14f);
    glVertex2f(0.7f,.14f);
    glEnd();
    //side color
      glBegin(GL_QUADS);
    glColor3ub(23, 32, 42  );
    glVertex2f(0.4f, .6f);
    glVertex2f(0.35f, .6f);
    glVertex2f(0.35f,.14f);
    glVertex2f(0.4f,.14f);
    glEnd();

     glBegin(GL_QUADS);
    glColor3ub(23, 32, 42  );
    glVertex2f(0.7f, .6f);
    glVertex2f(0.65f, .6f);
    glVertex2f(0.65f,.14f);
    glVertex2f(0.7f,.14f);
    glEnd();

    //floor

      glBegin(GL_QUADS);
    glColor3ub(1, 4, 4);
    glVertex2f(0.7f, .17f);
    glVertex2f(0.35f, .17f);
    glVertex2f(0.35f,.14f);
    glVertex2f(0.7f,.14f);
    glEnd();

      glBegin(GL_LINES);
    glColor3ub(133, 146, 158  );
    glVertex2f(0.35f, .34f);
    glVertex2f(0.7f, .34f);
    glEnd();

     glBegin(GL_LINES);
    glColor3ub(133, 146, 158  );
    glVertex2f(0.52f, .6f);
    glVertex2f(0.52f, .14f);
    glEnd();

    //left windows
    glBegin(GL_QUADS);
    glColor3ub(251, 252, 252);
    glVertex2f(0.5f, .3f);
    glVertex2f(0.37f, .3f);
    glVertex2f(0.37f,.2f);
    glVertex2f(0.5f,.2f);
    glEnd();

       glBegin(GL_QUADS);
    glColor3ub(93, 173, 226 );
    glVertex2f(0.49f, .29f);
    glVertex2f(0.38f, .29f);
    glVertex2f(0.38f,.21f);
    glVertex2f(0.49f,.21f);
    glEnd();

   glBegin(GL_QUADS);
    glColor3ub(251, 252, 252);
    glVertex2f(0.5f, .5f);
    glVertex2f(0.37f, .5f);
    glVertex2f(0.37f,.4f);
    glVertex2f(0.5f,.4f);
    glEnd();

    glBegin(GL_QUADS);
    glColor3ub(93, 173, 226);
    glVertex2f(0.49f, .49f);
    glVertex2f(0.38f, .49f);
    glVertex2f(0.38f,.41f);
    glVertex2f(0.49f,.41f);
    glEnd();


    //right windows

     glBegin(GL_QUADS);
    glColor3ub(251, 252, 252);
    glVertex2f(0.55f, .3f);
    glVertex2f(0.68f, .3f);
    glVertex2f(0.68f,.2f);
    glVertex2f(0.55f,.2f);
    glEnd();

     glBegin(GL_QUADS);
    glColor3ub(93, 173, 226);
    glVertex2f(0.56f, .29f);
    glVertex2f(0.67f, .29f);
    glVertex2f(0.67f,.21f);
    glVertex2f(0.56f,.21f);
    glEnd();

      glBegin(GL_QUADS);
    glColor3ub(251, 252, 252);
    glVertex2f(0.55f, .5f);
    glVertex2f(0.68f, .5f);
    glVertex2f(0.68f,.4f);
    glVertex2f(0.55f,.4f);
    glEnd();

       glBegin(GL_QUADS);
    glColor3ub(93, 173, 226);
    glVertex2f(0.56f, .49f);
    glVertex2f(0.67f, .49f);
    glVertex2f(0.67f,.41f);
    glVertex2f(0.56f,.41f);
    glEnd();

    //fifth building
      glBegin(GL_QUADS);
    glColor3ub(241, 196, 15 );
    glVertex2f(0.95f, .84f);
    glVertex2f(0.75f, .84f);
    glVertex2f(0.75f,.14f);
    glVertex2f(0.95f,.14f);
    glEnd();


     glBegin(GL_LINES);
    glColor3ub(251, 252, 252 );
    glVertex2f(0.75f, .24f);
    glVertex2f(0.95f, .24f);
    glEnd();


      glBegin(GL_LINES);
    glColor3ub(251, 252, 252 );
    glVertex2f(0.75f, .34f);
    glVertex2f(0.95f, .34f);
    glEnd();


      glBegin(GL_LINES);
    glColor3ub(251, 252, 252 );
    glVertex2f(0.75f, .44f);
    glVertex2f(0.95f, .44f);
    glEnd();

       glBegin(GL_LINES);
    glColor3ub(251, 252, 252 );
    glVertex2f(0.75f, .54f);
    glVertex2f(0.95f, .54f);
    glEnd();

     glBegin(GL_LINES);
    glColor3ub(251, 252, 252 );
    glVertex2f(0.75f, .64f);
    glVertex2f(0.95f, .64f);
    glEnd();

     glBegin(GL_LINES);
    glColor3ub(251, 252, 252 );
    glVertex2f(0.75f, .74f);
    glVertex2f(0.95f, .74f);
    glEnd();
}





//Flag
{


     //FLAG QUAD  2
    glBegin(GL_QUADS);
    glColor3ub(178,34,34);
    glVertex2f(-.08,.16);
    glVertex2f(-.082,.1);
    glVertex2f(.082,.1);
    glVertex2f(.08,.16);
    glEnd();

    //FLAG QUAD 1
    glBegin(GL_QUADS);
    glColor3ub(80,0,0);
    glVertex2f(-.06,.16);
    glVertex2f(-.06,.1);
    glVertex2f(.06,.1);
    glVertex2f(.06,.16);
    glEnd();

    //FLAG QUAD
    glBegin(GL_QUADS);
    glColor3ub(220,220,220);
    glVertex2f(-.08,.16);
    glVertex2f(-.082,.12);
    glVertex2f(-.06,.12);
    glVertex2f(-.06,.16);
    glEnd();

    //FLAG QUAD
    glBegin(GL_QUADS);
    glColor3ub(220,220,220);
    glVertex2f(.08,.16);
    glVertex2f(.082,.12);
    glVertex2f(.06,.12);
    glVertex2f(.06,.16);
    glEnd();





    //BD FLAG STAND
    glLineWidth(1);
    glBegin(GL_LINES);
    glColor3ub(238,232,170);
    glVertex2f(0,.16);
    glVertex2f(0,.3);
    glEnd();

    glBegin(GL_QUADS);
    glColor3ub(0,102,0);
    glVertex2f(0,.29);
    glVertex2f(0,.25);
    glVertex2f(.02,.24);
    glVertex2f(.025,.27);
    glEnd();


    //FLAG CIRCLE
     float x=0.01f,  y=.265f,  radius =.007f;
     float triangleAmount = 20;
	 float twicePi = 2.0f * PI;

	 glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(204,0,0);
		glVertex2f(x, y);
		for(int i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            x + (radius * cos(i *  twicePi / triangleAmount)),
			    y + (radius * sin(i * twicePi / triangleAmount))
			);
		}
	 glEnd();




}



//light
{

    //Left light
    glBegin(GL_QUADS);
    glColor3ub(20,20,20);
    glVertex2f(-.22,.23);
    glVertex2f(-.22,.13);
    glVertex2f(-.21,.13);
    glVertex2f(-.21,.23);
    glEnd();

    //Left light Top
    glBegin(GL_QUADS);
    glColor3ub(20,20,20);
    glVertex2f(-.22,.23);
    glVertex2f(-.21,.23);
    glVertex2f(-.18,.24);
    glVertex2f(-.2,.25);

    glVertex2f(-.21,.23);
    glVertex2f(-.22,.23);
    glVertex2f(-.26,.24);
    glVertex2f(-.23,.25);
    glEnd();


    //Right light
    glBegin(GL_QUADS);
    glColor3ub(20,20,20);
    glVertex2f(.22,.23);
    glVertex2f(.22,.13);
    glVertex2f(.21,.13);
    glVertex2f(.21,.23);
    glEnd();


    //Right light top
    glBegin(GL_QUADS);
    glColor3ub(20,20,20);
    glVertex2f(.22,.23);
    glVertex2f(.21,.23);
    glVertex2f(.18,.24);
    glVertex2f(.2,.25);

    glVertex2f(.21,.23);
    glVertex2f(.22,.23);
    glVertex2f(.26,.24);
    glVertex2f(.23,.25);
    glEnd();




}


    //BIRD
{
    glPushMatrix();
    glTranslatef(position3,0.0f, 0.0f);

    int i;
	GLfloat mm=0.182f; GLfloat nn=.801f; GLfloat radiusmm =.01f;
	float triangleAmount = 20;
	float twicePi = 2.0f * PI;

	glBegin(GL_TRIANGLE_FAN);
    glColor3ub(225, 225, 208);
    glVertex2f(mm, nn);
    for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            mm + (radiusmm * cos(i *  twicePi / triangleAmount)),
			    nn + (radiusmm * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();
    glBegin(GL_POLYGON);
    glColor3ub(225, 225, 208 );
    glVertex2f(0.1f,0.8f);
    glVertex2f(0.11f,0.79f);
    glVertex2f(0.12f,0.78f);
    glVertex2f(0.16f,0.77f);
    glVertex2f(0.19f,0.79f);
    glVertex2f(0.201f,0.8f);
    glEnd();

    glBegin(GL_TRIANGLES);
    glColor3ub(217, 217, 217);
    glVertex2f(0.175f,0.8f);
    glVertex2f(0.15f,0.8f);
    glVertex2f(0.14f,0.84f);
    glEnd();


    glBegin(GL_TRIANGLES);
    glColor3ub(242, 242, 242 );
    glVertex2f(0.175f,0.8f);
    glVertex2f(0.144f,0.8f);
    glVertex2f(0.12f,0.83f);
    glEnd();
	/////2nd bird////
	glBegin(GL_POLYGON);
    glColor3ub(225, 225, 208 );
    glVertex2f(-0.02f,0.8f);
    glVertex2f(-0.01f,0.79f);
    glVertex2f(0.0f,0.78f);
    glVertex2f(0.04f,0.77f);
    glVertex2f(0.07f,0.79f);
    glVertex2f(0.081f,0.8f);
    glEnd();

    glBegin(GL_TRIANGLES);
    glColor3ub(217, 217, 217);
    glVertex2f(0.055f,0.8f);
    glVertex2f(0.03f,0.8f);
    glVertex2f(0.02f,0.84f);
    glEnd();


    glBegin(GL_TRIANGLES);
    glColor3ub(242, 242, 242 );
    glVertex2f(0.055f,0.8f);
    glVertex2f(0.024f,0.8f);
    glVertex2f(0.0f,0.83f);
    glEnd();

	GLfloat mmm=0.062f; GLfloat nnn=.801f; GLfloat radiusmmm =.01f;

	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(225, 225, 208);
		glVertex2f(mmm, nnn);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            mmm + (radiusmmm * cos(i *  twicePi / triangleAmount)),
			    nnn + (radiusmmm * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();
	/////3rd bird/////
	glBegin(GL_POLYGON);
    glColor3ub(225, 225, 208 );
    glVertex2f(-0.72f,0.8f);
    glVertex2f(-0.71f,0.79f);
    glVertex2f(-0.7f,0.78f);
    glVertex2f(-0.66f,0.77f);
    glVertex2f(-0.63f,0.79f);
    glVertex2f(-0.619f,0.8f);
    glEnd();

    glBegin(GL_TRIANGLES);
    glColor3ub(217, 217, 217);
    glVertex2f(-0.645f,0.8f);
    glVertex2f(-0.67f,0.8f);
    glVertex2f(-0.68f,0.84f);
    glEnd();

    glBegin(GL_TRIANGLES);
    glColor3ub(242, 242, 242 );
    glVertex2f(-0.645f,0.8f);
    glVertex2f(-0.676f,0.8f);
    glVertex2f(-0.7f,0.83f);
    glEnd();

	GLfloat mmmm=-0.638f; GLfloat nnnn=.801f;

	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(225, 225, 208);
		glVertex2f(mmmm,nnnn);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            mmmm + (radiusmmm * cos(i *  twicePi / triangleAmount)),
			    nnnn + (radiusmmm * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();
	////4th bird////
	GLfloat mmmmm=-0.518f; GLfloat nnnnn=.801f;

	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(225, 225, 208);
		glVertex2f(mmmmm, nnnnn);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            mmmmm + (radiusmm * cos(i *  twicePi / triangleAmount)),
			    nnnnn + (radiusmm * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();
    glBegin(GL_POLYGON);
    glColor3ub(225, 225, 208 );
    glVertex2f(-0.6f,0.8f);
    glVertex2f(-0.59f,0.79f);
    glVertex2f(-0.58f,0.78f);
    glVertex2f(-0.54f,0.77f);
    glVertex2f(-0.51f,0.79f);
    glVertex2f(-0.499f,0.8f);
    glEnd();

    glBegin(GL_TRIANGLES);
    glColor3ub(217, 217, 217);
    glVertex2f(-0.525f,0.8f);
    glVertex2f(-0.55f,0.8f);
    glVertex2f(-0.56f,0.84f);
    glEnd();


    glBegin(GL_TRIANGLES);
    glColor3ub(242, 242, 242 );
    glVertex2f(-0.525f,0.8f);
    glVertex2f(-0.556f,0.8f);
    glVertex2f(-0.58f,0.83f);
    glEnd();









    //Bird-Copied
    {
    glPushMatrix();
    glTranslatef(.07,-.07,0);
    int i;
	GLfloat mm=0.182f; GLfloat nn=.801f; GLfloat radiusmm =.01f;
	triangleAmount = 20;
	twicePi = 2.0f * PI;

	glBegin(GL_TRIANGLE_FAN);
    glColor3ub(225, 225, 208);
    glVertex2f(mm, nn);
    for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            mm + (radiusmm * cos(i *  twicePi / triangleAmount)),
			    nn + (radiusmm * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();
    glBegin(GL_POLYGON);
    glColor3ub(225, 225, 208 );
    glVertex2f(0.1f,0.8f);
    glVertex2f(0.11f,0.79f);
    glVertex2f(0.12f,0.78f);
    glVertex2f(0.16f,0.77f);
    glVertex2f(0.19f,0.79f);
    glVertex2f(0.201f,0.8f);
    glEnd();

    glBegin(GL_TRIANGLES);
    glColor3ub(217, 217, 217);
    glVertex2f(0.175f,0.8f);
    glVertex2f(0.15f,0.8f);
    glVertex2f(0.14f,0.84f);
    glEnd();


    glBegin(GL_TRIANGLES);
    glColor3ub(242, 242, 242 );
    glVertex2f(0.175f,0.8f);
    glVertex2f(0.144f,0.8f);
    glVertex2f(0.12f,0.83f);
    glEnd();
	/////2nd bird////
	glBegin(GL_POLYGON);
    glColor3ub(225, 225, 208 );
    glVertex2f(-0.02f,0.8f);
    glVertex2f(-0.01f,0.79f);
    glVertex2f(0.0f,0.78f);
    glVertex2f(0.04f,0.77f);
    glVertex2f(0.07f,0.79f);
    glVertex2f(0.081f,0.8f);
    glEnd();

    glBegin(GL_TRIANGLES);
    glColor3ub(217, 217, 217);
    glVertex2f(0.055f,0.8f);
    glVertex2f(0.03f,0.8f);
    glVertex2f(0.02f,0.84f);
    glEnd();


    glBegin(GL_TRIANGLES);
    glColor3ub(242, 242, 242 );
    glVertex2f(0.055f,0.8f);
    glVertex2f(0.024f,0.8f);
    glVertex2f(0.0f,0.83f);
    glEnd();

	GLfloat mmm=0.062f; GLfloat nnn=.801f; GLfloat radiusmmm =.01f;

	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(225, 225, 208);
		glVertex2f(mmm, nnn);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            mmm + (radiusmmm * cos(i *  twicePi / triangleAmount)),
			    nnn + (radiusmmm * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();
	/////3rd bird/////
	glBegin(GL_POLYGON);
    glColor3ub(225, 225, 208 );
    glVertex2f(-0.72f,0.8f);
    glVertex2f(-0.71f,0.79f);
    glVertex2f(-0.7f,0.78f);
    glVertex2f(-0.66f,0.77f);
    glVertex2f(-0.63f,0.79f);
    glVertex2f(-0.619f,0.8f);
    glEnd();

    glBegin(GL_TRIANGLES);
    glColor3ub(217, 217, 217);
    glVertex2f(-0.645f,0.8f);
    glVertex2f(-0.67f,0.8f);
    glVertex2f(-0.68f,0.84f);
    glEnd();

    glBegin(GL_TRIANGLES);
    glColor3ub(242, 242, 242 );
    glVertex2f(-0.645f,0.8f);
    glVertex2f(-0.676f,0.8f);
    glVertex2f(-0.7f,0.83f);
    glEnd();

	GLfloat mmmm=-0.638f; GLfloat nnnn=.801f;

	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(225, 225, 208);
		glVertex2f(mmmm,nnnn);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            mmmm + (radiusmmm * cos(i *  twicePi / triangleAmount)),
			    nnnn + (radiusmmm * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();
	////4th bird////
	GLfloat mmmmm=-0.518f; GLfloat nnnnn=.801f;

	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(225, 225, 208);
		glVertex2f(mmmmm, nnnnn);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            mmmmm + (radiusmm * cos(i *  twicePi / triangleAmount)),
			    nnnnn + (radiusmm * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();


    glBegin(GL_POLYGON);
    glColor3ub(225, 225, 208 );
    glVertex2f(-0.6f,0.8f);
    glVertex2f(-0.59f,0.79f);
    glVertex2f(-0.58f,0.78f);
    glVertex2f(-0.54f,0.77f);
    glVertex2f(-0.51f,0.79f);
    glVertex2f(-0.499f,0.8f);
    glEnd();

    glBegin(GL_TRIANGLES);
    glColor3ub(217, 217, 217);
    glVertex2f(-0.525f,0.8f);
    glVertex2f(-0.55f,0.8f);
    glVertex2f(-0.56f,0.84f);
    glEnd();


    glBegin(GL_TRIANGLES);
    glColor3ub(242, 242, 242 );
    glVertex2f(-0.525f,0.8f);
    glVertex2f(-0.556f,0.8f);
    glVertex2f(-0.58f,0.83f);
    glEnd();
    glPopMatrix();
    }
glLoadIdentity();
	glPopMatrix();
}

//Base
{
     //Upper
    glBegin(GL_QUADS);
    glColor3ub(103,118,108);
    glVertex2f(-1,.07);
    glVertex2f(-1,.02);
    glVertex2f(1,.02);
    glVertex2f(1,.07);
    glEnd();
    //Mid
    glBegin(GL_QUADS);
    glColor3ub(147,35,12);
    glVertex2f(-1,.02);
    glVertex2f(-1,-.09);
    glVertex2f(1,-.09);
    glVertex2f(1,.02);
    glEnd();

    //Lower
    glBegin(GL_QUADS);
    glColor3ub(182,255,244);
    glVertex2f(-1,-.09);
    glVertex2f(-1,-.6);
    glVertex2f(1,-.6);
    glVertex2f(1,-.09);
    glEnd();
}

//Fish
{
    glPushMatrix();
    glTranslatef(_movef, -0.00f, 0.0f);

    glBegin(GL_POLYGON);
    glColor3d(0,0,0);
            glVertex3f(-.80f, -0.2f, 0.0f);
            glVertex3f(-.80f, -0.3f, 0.0f);
            glVertex3f(-.75f, -0.25f, 0.0f);
    glEnd();
    glBegin(GL_POLYGON);
            glVertex3f(-.75f, -0.225f, 0.0f);
            glVertex3f(-.75f, -0.275f, 0.0f);
            glVertex3f(-.70f, -0.275f, 0.0f);
            glVertex3f(-.70f, -0.225f, 0.0f);
    glEnd();
    glBegin(GL_POLYGON);
    glColor3d(0,0,1);
            glVertex3f(-.70f, -0.225f, 0.0f);
            glVertex3f(-.65f, -0.250f, 0.0f);
            glVertex3f(-.70f, -0.275f, 0.0f);
    glEnd();

	glPopMatrix();
    ///Fish///2
	glPushMatrix();
	glTranslatef(_movefb, -0.00f, 0.0f);
	glBegin(GL_POLYGON);
    glColor3d(0,0,0);
            glVertex3f(0.80f, -0.3f, 0.0f);
            glVertex3f(.80f, -0.4f, 0.0f);
            glVertex3f(.75f, -0.35f, 0.0f);
    glEnd();
    glBegin(GL_POLYGON);
            glVertex3f(.75f, -0.325f, 0.0f);
            glVertex3f(.75f, -0.375f, 0.0f);
            glVertex3f(.70f, -0.375f, 0.0f);
            glVertex3f(.70f, -0.325f, 0.0f);
    glEnd();
    glBegin(GL_POLYGON);
    glColor3d(0.5,0.2,0.7);
            glVertex3f(.70f, -0.325f, 0.0f);
            glVertex3f(.65f, -0.350f, 0.0f);
            glVertex3f(.70f, -0.375f, 0.0f);
    glEnd();

	glPopMatrix();
}



//Boat
{
     glPushMatrix();
     glTranslatef(_move3, 0.0f, 0.0f);
glBegin(GL_POLYGON);
     glColor3f(0.105, 0.086, 0.611);
//1 no
		glVertex2f(-.34,0);
		glVertex2f(-.37,-.1);
        glVertex2f(-.25,-.3);
		glVertex2f(-.15,-.3);
	glEnd();


	/* 2 no */
	glBegin(GL_POLYGON);
     glColor3f(0.866, 0.952, 0.952);

		glVertex2f(-.34,0);
		glVertex2f(-.4,.1);
        glVertex2f(-.45,0);
        glVertex2f(-.37,-.1);


	glEnd();
/* 3 no */
	glBegin(GL_POLYGON);
     glColor3f(0.866, 0.952, 0.952);

        glVertex2f(0,0);
        glVertex2f(-.1,0.1);
        glVertex2f(-.4,.1);
		glVertex2f(-.34,0);
		glVertex2f(-.1,0);
        glVertex2f(0,-.1);
        glVertex2f(.5,-.1);
		glVertex2f(.6,0);

	glEnd();
	/* 4 no */
	glBegin(GL_POLYGON);
     glColor3f(0.105, 0.086, 0.611);
        glVertex2f(0,-.1);
        glVertex2f(-.1,0);
        glVertex2f(-.34,0);
        glVertex2f(-.15,-.3);
        glVertex2f(.3,-.3);
        glVertex2f(.5,-.1);
        glVertex2f(0,-.1);
	glEnd();
/* 5 no */
	glBegin(GL_QUADS);
     glColor3f(0.043, 0.439, 0.835);

        glVertex2f(-.14,.23);
        glVertex2f(-.3,0.15);
        glVertex2f(-.3,.1);
        glVertex2f(-.14,.1);
	glEnd();


/* 6 no */
	glBegin(GL_POLYGON);
     glColor3f(0.415, 0.682, 0.945);
        glVertex2f(-.14,.23);
        glVertex2f(-.14,0.1);
        glVertex2f(-.1,.1);
        glVertex2f(0,0);
          glVertex2f(.55,0);
            glVertex2f(.55,0.05);

	glEnd();

//for 7
	glBegin(GL_QUADS);
     glColor3f(0.125, 0.082, 0.737);

        glVertex2f(-.15,.27);
        glVertex2f(-.28,0.22);
        glVertex2f(-.28,.16);
        glVertex2f(-.15,.22);
	glEnd();

	// for 8
	glBegin(GL_POLYGON);
     glColor3f(0.282, 0.321, 0.835);

        glVertex2f(-.15,.27);
        glVertex2f(-.15,.22);
        glVertex2f(-.14,0.23);
        glVertex2f(.53,.056);
        glVertex2f(.53,.1);
	glEnd();


	//for 9
	glBegin(GL_POLYGON);
     glColor3f(0.415, 0.682, 0.945);

        glVertex2f(.05,.35);
        glVertex2f(-.2,.3);
        glVertex2f(-.2,0.25);
        glVertex2f(-.15,.27);
        glVertex2f(.05,.217);
	glEnd();

	// for 10
	glBegin(GL_POLYGON);
     glColor3f(0.282, 0.607, 0.835);

         glVertex2f(.3,.35);
         glVertex2f(.05,.35);
         glVertex2f(.05,.217);
         glVertex2f(.4,.13);
          glVertex2f(.4,.4);
         glVertex2f(.3,.4);

	glEnd();



//11
glBegin(GL_POLYGON);
     glColor3f(0,0,0);

        glVertex2f(.15,.13);
        glVertex2f(0,.13);
        glVertex2f(0,0.05);
        glVertex2f(.15,.05);

	glEnd();

//12
	glBegin(GL_POLYGON);
     glColor3f(1,1,1);

        glVertex2f(.025,.11);
        glVertex2f(0.025,.075);
        glVertex2f(0.125,.075);
        glVertex2f(.125,.11);

	glEnd();

//1st line
glLineWidth(2);
    glBegin(GL_LINES);
    glColor3f(0.725, 0.250, 0.113);
    glVertex2f(.35,.4);
    glVertex2f(.35,.7);
    glEnd();
    //2nd line
glLineWidth(2);
    glBegin(GL_LINES);
    glColor3f(0.725, 0.250, 0.113);
    glVertex2f(.4,.4);
    glVertex2f(.35,.7);
    glEnd();
       //3rd line
glLineWidth(2);
    glBegin(GL_LINES);
    glColor3f(0.725, 0.250, 0.113);
    glVertex2f(.3,.4);
    glVertex2f(.35,.7);
    glEnd();
        //4th line
glLineWidth(2);
    glBegin(GL_LINES);
    glColor3f(0.725, 0.250, 0.113);
    glVertex2f(.05,.35);
    glVertex2f(.35,.7);
    glEnd();

             //5th line
glLineWidth(2);
    glBegin(GL_LINES);
    glColor3f(0.725, 0.250, 0.113);
    glVertex2f(.45,.7);
    glVertex2f(.25,.7);
    glEnd();

    glLineWidth(2);
    glBegin(GL_LINES);
    glColor3f(0.725, 0.250, 0.113);
    glVertex2f(.45,.65);
    glVertex2f(.25,.65);
    glEnd();

    glLineWidth(2);
    glBegin(GL_LINES);
    glColor3f(0.725, 0.250, 0.1130);
    glVertex2f(.45,.6);
    glVertex2f(.25,.6);
    glEnd();




//13
glBegin(GL_POLYGON);
     glColor3f(0,0,0);

        glVertex2f(.2,.1);
        glVertex2f(0.2,.03);
        glVertex2f(0.35,0.03);
        glVertex2f(.35,.1);

	glEnd();

	//14
glBegin(GL_POLYGON);
     glColor3f(1,1,1);

        glVertex2f(.22,.08);
        glVertex2f(0.22,.05);
        glVertex2f(0.33,0.05);
        glVertex2f(.33,.08);

	glEnd();


	//15
glBegin(GL_POLYGON);
     glColor3f(0,0,0);

        glVertex2f(.057,.3);
        glVertex2f(0.057,.25);
        glVertex2f(0.157,0.25);
        glVertex2f(.157,.3);

	glEnd();

	glBegin(GL_POLYGON);
     glColor3f(1,1,1);

        glVertex2f(.065,.28);
        glVertex2f(0.065,.265);
        glVertex2f(0.15,0.265);
        glVertex2f(.15,.28);

	glEnd();

	//16
glBegin(GL_POLYGON);
     glColor3f(0,0,0);

        glVertex2f(.2,.3);
        glVertex2f(0.2,.25);
        glVertex2f(0.3,0.25);
        glVertex2f(.3,.3);

	glEnd();



	glBegin(GL_POLYGON);
     glColor3f(1,1,1);

        glVertex2f(.21,.28);
        glVertex2f(0.21,.265);
        glVertex2f(0.29,0.265);
        glVertex2f(0.29,.28);

glEnd();



	//17
glBegin(GL_POLYGON);
     glColor3f(0,0,0);

        glVertex2f(.32,.25);
        glVertex2f(0.38,.25);
        glVertex2f(0.38,0.38);
        glVertex2f(.32,.38);

	glEnd();

	glBegin(GL_POLYGON);
     glColor3f(1,1,1);

        glVertex2f(.335,.265);
        glVertex2f(0.365,.265);
        glVertex2f(0.365,0.36);
        glVertex2f(.335,.36);

	glEnd();

	glBegin(GL_POLYGON);
     glColor3f(1,1,1);

        glVertex2f(.5,.105);
        glVertex2f(0.5,.5);
        glVertex2f(0.42,0.5);
        glVertex2f(0.42,.12);

	glEnd();



    //BD FLAG STAND
    glLineWidth(2);
    glBegin(GL_LINES);
    glColor3ub(238,232,170);
    glVertex2f(-.4,.1);
    glVertex2f(-.4,.4);
    glEnd();

    glBegin(GL_QUADS);
    glColor3ub(0,102,0);

    glVertex2f(-.4,.4);
    glVertex2f(-.4,.26);
    glVertex2f(-.21,.26);
    glVertex2f(-.21,.4);
    glEnd();


    //FLAG CIRCLE
     float x=-.3f,  y=.336f,  radius =.045f;
     float triangleAmount = 40;
	 float twicePi = 10.0f * PI;

	 glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(204,0,0);
		glVertex2f(x, y);
		for(int i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            x + (radius * cos(i *  twicePi / triangleAmount)),
			    y + (radius * sin(i * twicePi / triangleAmount))
			);
		}
	 glEnd();


       glPopMatrix();

}

//Fence
{
    //Fence-Left-1
    glPushMatrix();
    glScalef(.8,.7,0);
    glTranslatef(-.25,-.73,0);
    glLineWidth(3);
    glBegin(GL_LINES);
    glColor3ub(176, 176, 172);
    glVertex2f(-1.0f,-0.1f);
    glVertex2f(-0.6f,-0.1f);

    glVertex2f(-1.0f,-0.05f);
    glVertex2f(-0.6f,-0.05f);

    glVertex2f(-1.0f,0.0f);
    glVertex2f(-0.6f,0.0f);

    glVertex2f(-1.0f,0.05f);
    glVertex2f(-0.6f,0.05f);

    glVertex2f(-1.0f,0.1f);
    glVertex2f(-0.6f,0.1f);

    glVertex2f(-0.95f,0.13f);
    glVertex2f(-0.95f,-0.12f);

    glVertex2f(-0.9f,0.13f);
    glVertex2f(-0.9f,-0.12f);

    glVertex2f(-0.85f,0.13f);
    glVertex2f(-0.85f,-0.12f);

    glVertex2f(-0.8f,0.13f);
    glVertex2f(-0.8f,-0.12f);

    glVertex2f(-0.75f,0.13f);
    glVertex2f(-0.75f,-0.12f);

    glVertex2f(-0.7f,0.13f);
    glVertex2f(-0.7f,-0.12f);

    glVertex2f(-0.65f,0.13f);
    glVertex2f(-0.65f,-0.12f);

    glEnd();
    glPopMatrix();

    //Fence-Left-2
    glPushMatrix();
    glScalef(.8,.7,0);
    glTranslatef(.105,-.73,0);
    glLineWidth(3);
    glBegin(GL_LINES);
    glColor3ub(176, 176, 172);
    glVertex2f(-1.0f,-0.1f);
    glVertex2f(-0.6f,-0.1f);

    glVertex2f(-1.0f,-0.05f);
    glVertex2f(-0.6f,-0.05f);

    glVertex2f(-1.0f,0.0f);
    glVertex2f(-0.6f,0.0f);

    glVertex2f(-1.0f,0.05f);
    glVertex2f(-0.6f,0.05f);

    glVertex2f(-1.0f,0.1f);
    glVertex2f(-0.6f,0.1f);

    glVertex2f(-0.95f,0.13f);
    glVertex2f(-0.95f,-0.12f);

    glVertex2f(-0.9f,0.13f);
    glVertex2f(-0.9f,-0.12f);

    glVertex2f(-0.85f,0.13f);
    glVertex2f(-0.85f,-0.12f);

    glVertex2f(-0.8f,0.13f);
    glVertex2f(-0.8f,-0.12f);

    glVertex2f(-0.75f,0.13f);
    glVertex2f(-0.75f,-0.12f);

    glVertex2f(-0.7f,0.13f);
    glVertex2f(-0.7f,-0.12f);

    glVertex2f(-0.65f,0.13f);
    glVertex2f(-0.65f,-0.12f);

    glEnd();
    glPopMatrix();

    //Fence-Left-3
    glPushMatrix();
    glScalef(.8,.7,0);
    glTranslatef(.46,-.73,0);
    glLineWidth(3);
    glBegin(GL_LINES);
    glColor3ub(176, 176, 172);
    glVertex2f(-1.0f,-0.1f);
    glVertex2f(-0.6f,-0.1f);

    glVertex2f(-1.0f,-0.05f);
    glVertex2f(-0.6f,-0.05f);

    glVertex2f(-1.0f,0.0f);
    glVertex2f(-0.6f,0.0f);

    glVertex2f(-1.0f,0.05f);
    glVertex2f(-0.6f,0.05f);

    glVertex2f(-1.0f,0.1f);
    glVertex2f(-0.6f,0.1f);

    glVertex2f(-0.95f,0.13f);
    glVertex2f(-0.95f,-0.12f);

    glVertex2f(-0.9f,0.13f);
    glVertex2f(-0.9f,-0.12f);

    glVertex2f(-0.85f,0.13f);
    glVertex2f(-0.85f,-0.12f);

    glVertex2f(-0.8f,0.13f);
    glVertex2f(-0.8f,-0.12f);

    glVertex2f(-0.75f,0.13f);
    glVertex2f(-0.75f,-0.12f);

    glVertex2f(-0.7f,0.13f);
    glVertex2f(-0.7f,-0.12f);

    glVertex2f(-0.65f,0.13f);
    glVertex2f(-0.65f,-0.12f);

    glEnd();
    glPopMatrix();

    //Fence-Left-4
    glPushMatrix();
    glScalef(.8,.7,0);
    glTranslatef(.815,-.73,0);
    glLineWidth(3);
    glBegin(GL_LINES);
    glColor3ub(176, 176, 172);
    glVertex2f(-1.0f,-0.1f);
    glVertex2f(-0.6f,-0.1f);

    glVertex2f(-1.0f,-0.05f);
    glVertex2f(-0.6f,-0.05f);

    glVertex2f(-1.0f,0.0f);
    glVertex2f(-0.6f,0.0f);

    glVertex2f(-1.0f,0.05f);
    glVertex2f(-0.6f,0.05f);

    glVertex2f(-1.0f,0.1f);
    glVertex2f(-0.6f,0.1f);

    glVertex2f(-0.95f,0.13f);
    glVertex2f(-0.95f,-0.12f);

    glVertex2f(-0.9f,0.13f);
    glVertex2f(-0.9f,-0.12f);

    glVertex2f(-0.85f,0.13f);
    glVertex2f(-0.85f,-0.12f);

    glVertex2f(-0.8f,0.13f);
    glVertex2f(-0.8f,-0.12f);

    glVertex2f(-0.75f,0.13f);
    glVertex2f(-0.75f,-0.12f);

    glVertex2f(-0.7f,0.13f);
    glVertex2f(-0.7f,-0.12f);

    glVertex2f(-0.65f,0.13f);
    glVertex2f(-0.65f,-0.12f);

    glEnd();
    glPopMatrix();

    //Fence-Left-5
    glPushMatrix();
    glScalef(.8,.7,0);
    glTranslatef(1.17,-.73,0);
    glLineWidth(3);
    glBegin(GL_LINES);
    glColor3ub(176, 176, 172);
    glVertex2f(-1.0f,-0.1f);
    glVertex2f(-0.6f,-0.1f);

    glVertex2f(-1.0f,-0.05f);
    glVertex2f(-0.6f,-0.05f);

    glVertex2f(-1.0f,0.0f);
    glVertex2f(-0.6f,0.0f);

    glVertex2f(-1.0f,0.05f);
    glVertex2f(-0.6f,0.05f);

    glVertex2f(-1.0f,0.1f);
    glVertex2f(-0.6f,0.1f);

    glVertex2f(-0.95f,0.13f);
    glVertex2f(-0.95f,-0.12f);

    glVertex2f(-0.9f,0.13f);
    glVertex2f(-0.9f,-0.12f);

    glVertex2f(-0.85f,0.13f);
    glVertex2f(-0.85f,-0.12f);

    glVertex2f(-0.8f,0.13f);
    glVertex2f(-0.8f,-0.12f);

    glVertex2f(-0.75f,0.13f);
    glVertex2f(-0.75f,-0.12f);

    glVertex2f(-0.7f,0.13f);
    glVertex2f(-0.7f,-0.12f);

    glVertex2f(-0.65f,0.13f);
    glVertex2f(-0.65f,-0.12f);

    glEnd();
    glPopMatrix();

    //Fence-Left-6
    glPushMatrix();
    glScalef(.8,.7,0);
    glTranslatef(1.525,-.73,0);
    glLineWidth(3);
    glBegin(GL_LINES);
    glColor3ub(176, 176, 172);
    glVertex2f(-1.0f,-0.1f);
    glVertex2f(-0.6f,-0.1f);

    glVertex2f(-1.0f,-0.05f);
    glVertex2f(-0.6f,-0.05f);

    glVertex2f(-1.0f,0.0f);
    glVertex2f(-0.6f,0.0f);

    glVertex2f(-1.0f,0.05f);
    glVertex2f(-0.6f,0.05f);

    glVertex2f(-1.0f,0.1f);
    glVertex2f(-0.6f,0.1f);

    glVertex2f(-0.95f,0.13f);
    glVertex2f(-0.95f,-0.12f);

    glVertex2f(-0.9f,0.13f);
    glVertex2f(-0.9f,-0.12f);

    glVertex2f(-0.85f,0.13f);
    glVertex2f(-0.85f,-0.12f);

    glVertex2f(-0.8f,0.13f);
    glVertex2f(-0.8f,-0.12f);

    glVertex2f(-0.75f,0.13f);
    glVertex2f(-0.75f,-0.12f);

    glVertex2f(-0.7f,0.13f);
    glVertex2f(-0.7f,-0.12f);

    glVertex2f(-0.65f,0.13f);
    glVertex2f(-0.65f,-0.12f);

    glEnd();
    glPopMatrix();

    //Fence-Left-7
    glPushMatrix();
    glScalef(.8,.7,0);
    glTranslatef(1.88,-.73,0);
    glLineWidth(3);
    glBegin(GL_LINES);
    glColor3ub(176, 176, 172);
    glVertex2f(-1.0f,-0.1f);
    glVertex2f(-0.6f,-0.1f);

    glVertex2f(-1.0f,-0.05f);
    glVertex2f(-0.6f,-0.05f);

    glVertex2f(-1.0f,0.0f);
    glVertex2f(-0.6f,0.0f);

    glVertex2f(-1.0f,0.05f);
    glVertex2f(-0.6f,0.05f);

    glVertex2f(-1.0f,0.1f);
    glVertex2f(-0.6f,0.1f);

    glVertex2f(-0.95f,0.13f);
    glVertex2f(-0.95f,-0.12f);

    glVertex2f(-0.9f,0.13f);
    glVertex2f(-0.9f,-0.12f);

    glVertex2f(-0.85f,0.13f);
    glVertex2f(-0.85f,-0.12f);

    glVertex2f(-0.8f,0.13f);
    glVertex2f(-0.8f,-0.12f);

    glVertex2f(-0.75f,0.13f);
    glVertex2f(-0.75f,-0.12f);

    glVertex2f(-0.7f,0.13f);
    glVertex2f(-0.7f,-0.12f);

    glVertex2f(-0.65f,0.13f);
    glVertex2f(-0.65f,-0.12f);

    glEnd();
    glPopMatrix();

}



    //FootWalk
    glBegin(GL_QUADS);
    glColor3ub(255,178,102);
    glVertex2f(-1,-.6);
    glVertex2f(-1,-.66);
    glVertex2f(1,-.66);
    glVertex2f(1,-.6);
    glEnd();





//Road side tree
{
    //Left-1
    glPushMatrix();
    glScalef(.5,.4,0);
    glTranslatef(-.9,-1.4,0);
    glBegin(GL_POLYGON);
    glColor3ub(102, 51, 0);
    glVertex2f(-0.72f,-0.15f);
    glVertex2f(-0.65f,-0.2f);
    glVertex2f(-0.735f,-0.17f);
    glVertex2f(-0.74f,-0.25f);
    glVertex2f(-0.775f,-0.17f);
    glVertex2f(-0.85f,-0.2f);
    glVertex2f(-0.78f,-0.15f);
    glEnd();

    glBegin(GL_QUADS);
    glColor3ub(102, 51, 0);
    glVertex2f(-0.78f,-0.15f);
    glVertex2f(-0.78f,0.23f);
    glVertex2f(-0.72f,0.23f);
    glVertex2f(-0.72f,-0.15f);
    glEnd();
    glBegin(GL_QUADS);
    glColor3ub(102, 51, 0);
    glVertex2f(-0.76f,0.23f);
    glVertex2f(-0.76f,0.3f);
    glVertex2f(-0.74f,0.3f);
    glVertex2f(-0.74f,0.23f);
    glEnd();
    glBegin(GL_QUADS);
    glColor3ub(102, 51, 0);
    glVertex2f(-0.74f,0.23f);
    glVertex2f(-0.71f,0.29f);
    glVertex2f(-0.7f,0.28f);
    glVertex2f(-0.72f,0.23f);
    glEnd();
    glBegin(GL_QUADS);
    glColor3ub(102, 51, 0);
    glVertex2f(-0.78f,0.23f);
    glVertex2f(-0.8f,0.28f);
    glVertex2f(-0.79f,0.29f);
    glVertex2f(-0.76f,0.23f);
    glEnd();

    int i;

	 float x=-.75f,  y=.33f,  radius =.06f;
	float triangleAmount = 20;
    float twicePi = 2.0f * PI;

	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(51, 204, 51);
		glVertex2f(x, y);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            x + (radius * cos(i *  twicePi / triangleAmount)),
			    y + (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();

    GLfloat a=-.68f; GLfloat b=.31f;

	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(51, 204, 51);
		glVertex2f(a, b);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            a + (radius * cos(i *  twicePi / triangleAmount)),
			    b + (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();

	GLfloat c=-.81f; GLfloat d=.31f;

	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(51, 204, 51);
		glVertex2f(c, d);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            c + (radius * cos(i *  twicePi / triangleAmount)),
			    d + (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();

	GLfloat e=-.87f; GLfloat f=.35f;

	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(51, 204, 51);
		glVertex2f(e, f);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            e + (radius * cos(i *  twicePi / triangleAmount)),
			    f+ (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();

	GLfloat g=-.61f; GLfloat h=.35f;

	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(51, 204, 51);
		glVertex2f(g, h);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            g + (radius * cos(i *  twicePi / triangleAmount)),
			    h+ (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();
	GLfloat a1=-.61f; GLfloat b1=.4f;

	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(51, 204, 51);
		glVertex2f(a1, b1);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            a1 + (radius * cos(i *  twicePi / triangleAmount)),
			    b1 + (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();

	GLfloat c1=-.88f; GLfloat d1=.4f;

	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(51, 204, 51);
		glVertex2f(c, d);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            c1 + (radius * cos(i *  twicePi / triangleAmount)),
			    d1 + (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();

	GLfloat e1=-.87f; GLfloat f1=.44f;

	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(51, 204, 51);
		glVertex2f(e1, f1);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            e1 + (radius * cos(i *  twicePi / triangleAmount)),
			    f1+ (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();

	GLfloat g1=-.61f; GLfloat h1=.4f;

	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(51, 204, 51);
		glVertex2f(g, h);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            g1 + (radius * cos(i *  twicePi / triangleAmount)),
			    h1+ (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();

	GLfloat e11=-.64f; GLfloat f11=.44f;
	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(51, 204, 51);
		glVertex2f(e11, f11);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            e11 + (radius * cos(i *  twicePi / triangleAmount)),
			    f11+ (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();

	GLfloat e12=-.75f; GLfloat f12=.44f;
	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(51, 204, 51);
		glVertex2f(e12, f12);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            e12 + (radius * cos(i *  twicePi / triangleAmount)),
			    f12+ (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();

    glBegin(GL_QUADS);
    glColor3ub(51, 204, 51);
    glVertex2f(-0.85f,0.33f);
    glVertex2f(-0.85f,0.44f);
    glVertex2f(-0.65f,0.44f);
    glVertex2f(-0.65f,0.33f);
    glEnd();

    GLfloat e123=-.8f; GLfloat f123=.5f;
	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(51, 204, 51);
		glVertex2f(e123, f123);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            e123 + (radius * cos(i *  twicePi / triangleAmount)),
			    f123+ (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();
	GLfloat e1232=-.7f; GLfloat f1232=.5f;

	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(51, 204, 51);
		glVertex2f(e1232, f1232);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            e1232 + (radius * cos(i *  twicePi / triangleAmount)),
			    f1232+ (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();
	glPopMatrix();


	//Left-2
    glPushMatrix();
    glScalef(.5,.4,0);
    glTranslatef(.35,-1.4,0);
    glBegin(GL_POLYGON);
    glColor3ub(102, 51, 0);
    glVertex2f(-0.72f,-0.15f);
    glVertex2f(-0.65f,-0.2f);
    glVertex2f(-0.735f,-0.17f);
    glVertex2f(-0.74f,-0.25f);
    glVertex2f(-0.775f,-0.17f);
    glVertex2f(-0.85f,-0.2f);
    glVertex2f(-0.78f,-0.15f);
    glEnd();

    glBegin(GL_QUADS);
    glColor3ub(102, 51, 0);
    glVertex2f(-0.78f,-0.15f);
    glVertex2f(-0.78f,0.23f);
    glVertex2f(-0.72f,0.23f);
    glVertex2f(-0.72f,-0.15f);
    glEnd();
    glBegin(GL_QUADS);
    glColor3ub(102, 51, 0);
    glVertex2f(-0.76f,0.23f);
    glVertex2f(-0.76f,0.3f);
    glVertex2f(-0.74f,0.3f);
    glVertex2f(-0.74f,0.23f);
    glEnd();
    glBegin(GL_QUADS);
    glColor3ub(102, 51, 0);
    glVertex2f(-0.74f,0.23f);
    glVertex2f(-0.71f,0.29f);
    glVertex2f(-0.7f,0.28f);
    glVertex2f(-0.72f,0.23f);
    glEnd();
    glBegin(GL_QUADS);
    glColor3ub(102, 51, 0);
    glVertex2f(-0.78f,0.23f);
    glVertex2f(-0.8f,0.28f);
    glVertex2f(-0.79f,0.29f);
    glVertex2f(-0.76f,0.23f);
    glEnd();


	 x=-.75f;  y=.33f;  radius =.06f;
	triangleAmount = 20;
    twicePi = 2.0f * PI;

	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(51, 204, 51);
		glVertex2f(x, y);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            x + (radius * cos(i *  twicePi / triangleAmount)),
			    y + (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();

    a=-.68f;  b=.31f;

	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(51, 204, 51);
		glVertex2f(a, b);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            a + (radius * cos(i *  twicePi / triangleAmount)),
			    b + (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();

	 c=-.81f;  d=.31f;

	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(51, 204, 51);
		glVertex2f(c, d);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            c + (radius * cos(i *  twicePi / triangleAmount)),
			    d + (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();

	 e=-.87f;  f=.35f;

	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(51, 204, 51);
		glVertex2f(e, f);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            e + (radius * cos(i *  twicePi / triangleAmount)),
			    f+ (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();

	 g=-.61f;  h=.35f;

	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(51, 204, 51);
		glVertex2f(g, h);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            g + (radius * cos(i *  twicePi / triangleAmount)),
			    h+ (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();
	 a1=-.61f;  b1=.4f;

	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(51, 204, 51);
		glVertex2f(a1, b1);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            a1 + (radius * cos(i *  twicePi / triangleAmount)),
			    b1 + (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();

	 c1=-.88f;  d1=.4f;

	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(51, 204, 51);
		glVertex2f(c, d);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            c1 + (radius * cos(i *  twicePi / triangleAmount)),
			    d1 + (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();

	 e1=-.87f;  f1=.44f;

	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(51, 204, 51);
		glVertex2f(e1, f1);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            e1 + (radius * cos(i *  twicePi / triangleAmount)),
			    f1+ (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();

	 g1=-.61f;  h1=.4f;

	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(51, 204, 51);
		glVertex2f(g, h);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            g1 + (radius * cos(i *  twicePi / triangleAmount)),
			    h1+ (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();

	 e11=-.64f;  f11=.44f;
	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(51, 204, 51);
		glVertex2f(e11, f11);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            e11 + (radius * cos(i *  twicePi / triangleAmount)),
			    f11+ (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();

	 e12=-.75f;  f12=.44f;
	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(51, 204, 51);
		glVertex2f(e12, f12);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            e12 + (radius * cos(i *  twicePi / triangleAmount)),
			    f12+ (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();

    glBegin(GL_QUADS);
    glColor3ub(51, 204, 51);
    glVertex2f(-0.85f,0.33f);
    glVertex2f(-0.85f,0.44f);
    glVertex2f(-0.65f,0.44f);
    glVertex2f(-0.65f,0.33f);
    glEnd();

    e123=-.8f;  f123=.5f;
	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(51, 204, 51);
		glVertex2f(e123, f123);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            e123 + (radius * cos(i *  twicePi / triangleAmount)),
			    f123+ (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();
	 e1232=-.7f;  f1232=.5f;

	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(51, 204, 51);
		glVertex2f(e1232, f1232);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            e1232 + (radius * cos(i *  twicePi / triangleAmount)),
			    f1232+ (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();
	glPopMatrix();

	//Left-3
    glPushMatrix();
    glScalef(.5,.4,0);
    glTranslatef(1.6,-1.4,0);
    glBegin(GL_POLYGON);
    glColor3ub(102, 51, 0);
    glVertex2f(-0.72f,-0.15f);
    glVertex2f(-0.65f,-0.2f);
    glVertex2f(-0.735f,-0.17f);
    glVertex2f(-0.74f,-0.25f);
    glVertex2f(-0.775f,-0.17f);
    glVertex2f(-0.85f,-0.2f);
    glVertex2f(-0.78f,-0.15f);
    glEnd();

    glBegin(GL_QUADS);
    glColor3ub(102, 51, 0);
    glVertex2f(-0.78f,-0.15f);
    glVertex2f(-0.78f,0.23f);
    glVertex2f(-0.72f,0.23f);
    glVertex2f(-0.72f,-0.15f);
    glEnd();
    glBegin(GL_QUADS);
    glColor3ub(102, 51, 0);
    glVertex2f(-0.76f,0.23f);
    glVertex2f(-0.76f,0.3f);
    glVertex2f(-0.74f,0.3f);
    glVertex2f(-0.74f,0.23f);
    glEnd();
    glBegin(GL_QUADS);
    glColor3ub(102, 51, 0);
    glVertex2f(-0.74f,0.23f);
    glVertex2f(-0.71f,0.29f);
    glVertex2f(-0.7f,0.28f);
    glVertex2f(-0.72f,0.23f);
    glEnd();
    glBegin(GL_QUADS);
    glColor3ub(102, 51, 0);
    glVertex2f(-0.78f,0.23f);
    glVertex2f(-0.8f,0.28f);
    glVertex2f(-0.79f,0.29f);
    glVertex2f(-0.76f,0.23f);
    glEnd();


	 x=-.75f;  y=.33f;  radius =.06f;
	triangleAmount = 20;
    twicePi = 2.0f * PI;

	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(51, 204, 51);
		glVertex2f(x, y);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            x + (radius * cos(i *  twicePi / triangleAmount)),
			    y + (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();

    a=-.68f;  b=.31f;

	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(51, 204, 51);
		glVertex2f(a, b);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            a + (radius * cos(i *  twicePi / triangleAmount)),
			    b + (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();

	 c=-.81f;  d=.31f;

	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(51, 204, 51);
		glVertex2f(c, d);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            c + (radius * cos(i *  twicePi / triangleAmount)),
			    d + (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();

	 e=-.87f;  f=.35f;

	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(51, 204, 51);
		glVertex2f(e, f);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            e + (radius * cos(i *  twicePi / triangleAmount)),
			    f+ (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();

	 g=-.61f;  h=.35f;

	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(51, 204, 51);
		glVertex2f(g, h);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            g + (radius * cos(i *  twicePi / triangleAmount)),
			    h+ (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();
	 a1=-.61f;  b1=.4f;

	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(51, 204, 51);
		glVertex2f(a1, b1);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            a1 + (radius * cos(i *  twicePi / triangleAmount)),
			    b1 + (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();

	 c1=-.88f;  d1=.4f;

	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(51, 204, 51);
		glVertex2f(c, d);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            c1 + (radius * cos(i *  twicePi / triangleAmount)),
			    d1 + (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();

	 e1=-.87f;  f1=.44f;

	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(51, 204, 51);
		glVertex2f(e1, f1);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            e1 + (radius * cos(i *  twicePi / triangleAmount)),
			    f1+ (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();

	 g1=-.61f;  h1=.4f;

	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(51, 204, 51);
		glVertex2f(g, h);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            g1 + (radius * cos(i *  twicePi / triangleAmount)),
			    h1+ (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();

	 e11=-.64f;  f11=.44f;
	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(51, 204, 51);
		glVertex2f(e11, f11);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            e11 + (radius * cos(i *  twicePi / triangleAmount)),
			    f11+ (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();

	 e12=-.75f;  f12=.44f;
	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(51, 204, 51);
		glVertex2f(e12, f12);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            e12 + (radius * cos(i *  twicePi / triangleAmount)),
			    f12+ (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();

    glBegin(GL_QUADS);
    glColor3ub(51, 204, 51);
    glVertex2f(-0.85f,0.33f);
    glVertex2f(-0.85f,0.44f);
    glVertex2f(-0.65f,0.44f);
    glVertex2f(-0.65f,0.33f);
    glEnd();

    e123=-.8f;  f123=.5f;
	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(51, 204, 51);
		glVertex2f(e123, f123);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            e123 + (radius * cos(i *  twicePi / triangleAmount)),
			    f123+ (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();
	 e1232=-.7f;  f1232=.5f;

	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(51, 204, 51);
		glVertex2f(e1232, f1232);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            e1232 + (radius * cos(i *  twicePi / triangleAmount)),
			    f1232+ (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();
	glPopMatrix();

	//Left-4
    glPushMatrix();
    glScalef(.5,.4,0);
    glTranslatef(2.5,-1.4,0);
    glBegin(GL_POLYGON);
    glColor3ub(102, 51, 0);
    glVertex2f(-0.72f,-0.15f);
    glVertex2f(-0.65f,-0.2f);
    glVertex2f(-0.735f,-0.17f);
    glVertex2f(-0.74f,-0.25f);
    glVertex2f(-0.775f,-0.17f);
    glVertex2f(-0.85f,-0.2f);
    glVertex2f(-0.78f,-0.15f);
    glEnd();

    glBegin(GL_QUADS);
    glColor3ub(102, 51, 0);
    glVertex2f(-0.78f,-0.15f);
    glVertex2f(-0.78f,0.23f);
    glVertex2f(-0.72f,0.23f);
    glVertex2f(-0.72f,-0.15f);
    glEnd();
    glBegin(GL_QUADS);
    glColor3ub(102, 51, 0);
    glVertex2f(-0.76f,0.23f);
    glVertex2f(-0.76f,0.3f);
    glVertex2f(-0.74f,0.3f);
    glVertex2f(-0.74f,0.23f);
    glEnd();
    glBegin(GL_QUADS);
    glColor3ub(102, 51, 0);
    glVertex2f(-0.74f,0.23f);
    glVertex2f(-0.71f,0.29f);
    glVertex2f(-0.7f,0.28f);
    glVertex2f(-0.72f,0.23f);
    glEnd();
    glBegin(GL_QUADS);
    glColor3ub(102, 51, 0);
    glVertex2f(-0.78f,0.23f);
    glVertex2f(-0.8f,0.28f);
    glVertex2f(-0.79f,0.29f);
    glVertex2f(-0.76f,0.23f);
    glEnd();


	 x=-.75f;  y=.33f;  radius =.06f;
	triangleAmount = 20;
    twicePi = 2.0f * PI;

	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(51, 204, 51);
		glVertex2f(x, y);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            x + (radius * cos(i *  twicePi / triangleAmount)),
			    y + (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();

    a=-.68f;  b=.31f;

	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(51, 204, 51);
		glVertex2f(a, b);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            a + (radius * cos(i *  twicePi / triangleAmount)),
			    b + (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();

	 c=-.81f;  d=.31f;

	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(51, 204, 51);
		glVertex2f(c, d);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            c + (radius * cos(i *  twicePi / triangleAmount)),
			    d + (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();

	 e=-.87f;  f=.35f;

	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(51, 204, 51);
		glVertex2f(e, f);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            e + (radius * cos(i *  twicePi / triangleAmount)),
			    f+ (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();

	 g=-.61f;  h=.35f;

	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(51, 204, 51);
		glVertex2f(g, h);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            g + (radius * cos(i *  twicePi / triangleAmount)),
			    h+ (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();
	 a1=-.61f;  b1=.4f;

	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(51, 204, 51);
		glVertex2f(a1, b1);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            a1 + (radius * cos(i *  twicePi / triangleAmount)),
			    b1 + (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();

	 c1=-.88f;  d1=.4f;

	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(51, 204, 51);
		glVertex2f(c, d);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            c1 + (radius * cos(i *  twicePi / triangleAmount)),
			    d1 + (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();

	 e1=-.87f;  f1=.44f;

	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(51, 204, 51);
		glVertex2f(e1, f1);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            e1 + (radius * cos(i *  twicePi / triangleAmount)),
			    f1+ (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();

	 g1=-.61f;  h1=.4f;

	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(51, 204, 51);
		glVertex2f(g, h);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            g1 + (radius * cos(i *  twicePi / triangleAmount)),
			    h1+ (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();

	 e11=-.64f;  f11=.44f;
	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(51, 204, 51);
		glVertex2f(e11, f11);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            e11 + (radius * cos(i *  twicePi / triangleAmount)),
			    f11+ (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();

	 e12=-.75f;  f12=.44f;
	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(51, 204, 51);
		glVertex2f(e12, f12);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            e12 + (radius * cos(i *  twicePi / triangleAmount)),
			    f12+ (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();

    glBegin(GL_QUADS);
    glColor3ub(51, 204, 51);
    glVertex2f(-0.85f,0.33f);
    glVertex2f(-0.85f,0.44f);
    glVertex2f(-0.65f,0.44f);
    glVertex2f(-0.65f,0.33f);
    glEnd();

    e123=-.8f;  f123=.5f;
	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(51, 204, 51);
		glVertex2f(e123, f123);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            e123 + (radius * cos(i *  twicePi / triangleAmount)),
			    f123+ (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();
	 e1232=-.7f;  f1232=.5f;

	glBegin(GL_TRIANGLE_FAN);
	    glColor3ub(51, 204, 51);
		glVertex2f(e1232, f1232);
		for(i = 0; i <= triangleAmount;i++) {
			glVertex2f(
		            e1232 + (radius * cos(i *  twicePi / triangleAmount)),
			    f1232+ (radius * sin(i * twicePi / triangleAmount))
			);
		}
	glEnd();
	glPopMatrix();




//LIGHT Left
    glPushMatrix();
    glTranslatef(-.3,-.65,0);

    glBegin(GL_QUADS);
    glColor3ub(20,20,20);
    glVertex2f(-.22,.23);
    glVertex2f(-.22,.02);
    glVertex2f(-.21,.02);
    glVertex2f(-.21,.23);
    glEnd();


    //LIGHT Left Top Two
    glBegin(GL_QUADS);
    glColor3ub(20,20,20);
    glVertex2f(-.22,.23);
    glVertex2f(-.21,.23);
    glVertex2f(-.18,.24);
    glVertex2f(-.2,.25);

    glVertex2f(-.21,.23);
    glVertex2f(-.22,.23);
    glVertex2f(-.26,.24);
    glVertex2f(-.23,.25);
    glEnd();
    glLoadIdentity();
    glPopMatrix();


    //LIGHT Right
    glPushMatrix();
    glTranslatef(0,-.65,0);
    glBegin(GL_QUADS);
    glColor3ub(20,20,20);
    glVertex2f(.22,.23);
    glVertex2f(.22,.02);
    glVertex2f(.21,.02);
    glVertex2f(.21,.23);
    glEnd();


    //LIGHT Right Top Two

    glBegin(GL_QUADS);
    glColor3ub(20,20,20);
    glVertex2f(.22,.23);
    glVertex2f(.21,.23);
    glVertex2f(.18,.24);
    glVertex2f(.2,.25);

    glVertex2f(.21,.23);
    glVertex2f(.22,.23);
    glVertex2f(.26,.24);
    glVertex2f(.23,.25);
    glEnd();
    glLoadIdentity();
    glPopMatrix();







//LIGHT Left
    glPushMatrix();
    glTranslatef(-.75,-.65,0);

    glBegin(GL_QUADS);
    glColor3ub(20,20,20);
    glVertex2f(-.22,.23);
    glVertex2f(-.22,.02);
    glVertex2f(-.21,.02);
    glVertex2f(-.21,.23);
    glEnd();


    //LIGHT Left Top Two
    glBegin(GL_QUADS);
    glColor3ub(20,20,20);
    glVertex2f(-.22,.23);
    glVertex2f(-.21,.23);
    glVertex2f(-.18,.24);
    glVertex2f(-.2,.25);

    glVertex2f(-.21,.23);
    glVertex2f(-.22,.23);
    glVertex2f(-.26,.24);
    glVertex2f(-.23,.25);
    glEnd();
    glLoadIdentity();
    glPopMatrix();


    //LIGHT Right
    glPushMatrix();
    glTranslatef(.5,-.65,0);
    glBegin(GL_QUADS);
    glColor3ub(20,20,20);
    glVertex2f(.22,.23);
    glVertex2f(.22,.02);
    glVertex2f(.21,.02);
    glVertex2f(.21,.23);
    glEnd();


    //LIGHT Right Top Two

    glBegin(GL_QUADS);
    glColor3ub(20,20,20);
    glVertex2f(.22,.23);
    glVertex2f(.21,.23);
    glVertex2f(.18,.24);
    glVertex2f(.2,.25);

    glVertex2f(.21,.23);
    glVertex2f(.22,.23);
    glVertex2f(.26,.24);
    glVertex2f(.23,.25);
    glEnd();
    glLoadIdentity();
    glPopMatrix();

}



//Upper Car
{
    int i;

    glPushMatrix();
    glTranslatef(position,0.0f, 0.0f);
    glTranslatef(0,-.38,0);
    glBegin(GL_POLYGON);
    glColor3ub(128,0,0);
    glVertex2f(.04,-.24);
    glVertex2f(0.0,-.34);
    glVertex2f(0,-.40);
    glVertex2f(.4,-.40);
    glVertex2f(.4,-.24);
    glEnd();

    glBegin(GL_QUADS);
    glColor3ub(240,255,240);
    glVertex2f(.37,-.26);
    glVertex2f(.30,-.26);
    glVertex2f(.30,-.34);
    glVertex2f(.37,-.34);
    glEnd();

    glBegin(GL_QUADS);
    glColor3ub(240,255,240);
    glVertex2f(.28,-.26);
    glVertex2f(.22,-.26);
    glVertex2f(.22,-.34);
    glVertex2f(.28,-.34);
    glEnd();

    glBegin(GL_QUADS);
    glColor3ub(240,255,240);
    glVertex2f(.20,-.26);
    glVertex2f(.14,-.26);
    glVertex2f(.14,-.34);
    glVertex2f(.20,-.34);
    glEnd();

    glBegin(GL_QUADS);
    glColor3ub(240,255,240);
    glVertex2f(.12,-.26);
    glVertex2f(.05,-.26);
    glVertex2f(.02,-.34);
    glVertex2f(.12,-.34);
    glEnd();
//car wheel front
	x=.08f;  y=-.40f;  radius =.04f;
    triangleAmount = 20;
    twicePi = 2.0f * PI;

	glBegin(GL_TRIANGLE_FAN);
	glColor3ub(0,0,0);
    glVertex2f(x, y);
    for(i = 0; i <= triangleAmount;i++)
    {
        glVertex2f
        (
                x + (radius * cos(i *  twicePi / triangleAmount)),
			    y + (radius * sin(i * twicePi / triangleAmount))
        );
    }
	glEnd();
//-----------------
	x=.08f;  y=-.40f;  radius =.025f;
    triangleAmount = 20;
    twicePi = 2.0f * PI;

	glBegin(GL_TRIANGLE_FAN);
	glColor3ub(255,250,250);
    glVertex2f(x, y);
    for(i = 0; i <= triangleAmount;i++)
    {
        glVertex2f
        (
                x + (radius * cos(i *  twicePi / triangleAmount)),
			    y + (radius * sin(i * twicePi / triangleAmount))
        );
    }
	glEnd();
//car wheel back
	x=.3f;  y=-.40f;  radius =.04f;
    triangleAmount = 20;
    twicePi = 2.0f * PI;

	glBegin(GL_TRIANGLE_FAN);
	glColor3ub(0,0,0);
    glVertex2f(x, y);
    for(i = 0; i <= triangleAmount;i++)
    {
        glVertex2f
        (
                x + (radius * cos(i *  twicePi / triangleAmount)),
			    y + (radius * sin(i * twicePi / triangleAmount))
        );
    }
	glEnd();
//-----------------
	x=.3f;  y=-.40f;  radius =.025f;
    triangleAmount = 20;
    twicePi = 2.0f * PI;

	glBegin(GL_TRIANGLE_FAN);
	glColor3ub(255,250,250);
    glVertex2f(x, y);
    for(i = 0; i <= triangleAmount;i++)
    {
        glVertex2f
        (
                x + (radius * cos(i *  twicePi / triangleAmount)),
			    y + (radius * sin(i * twicePi / triangleAmount))
        );
    }
	glEnd();
	glLoadIdentity();
    glPopMatrix();


}





    //glutTimerFunc(8000,night,0);

	glFlush();


}
void display()
{
    glutDisplayFunc(day);
}

int main(int argc, char** argv)
{
	glutInit(&argc, argv);
    glutInitWindowSize(960,640);
    glutInitWindowPosition(220 ,340);
    glutCreateWindow("Final");
    init();
	glutDisplayFunc(display);
	glutIdleFunc(idle);

	glutTimerFunc(50, updateauto, 0);

	//glutTimerFunc(200, update, 0);
	//glutTimerFunc(200, update2, 0);
    glutTimerFunc(100, update3, 0);
    glutTimerFunc(100, update4, 0);

    glutSpecialFunc(SpecialInput);
    glutKeyboardFunc(handleKeypress);

	glutMainLoop();
	return 0;
}

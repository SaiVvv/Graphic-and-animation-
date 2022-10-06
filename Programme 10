#include "gl/glut.h"
#include <gl/gl.h>

void Display(void)
{
	glClear(GL_COLOR_BUFFER_BIT | GL_DEPTH_BUFFER_BIT);
	glLoadIdentity();
	gluLookAt(0.0, 0.0, 5.0, 0.0, 0.0, 0.0, 0.0, 1.0, 0.0);
	 glColor3f(0.0, 1.0, 0.0);
	glBegin(GL_POLYGON);
 		glVertex3f( 0.0, 0.0, 0.0); // V0 ( 0, 0, 0)
 		glVertex3f( 1.0f, 0.0, 0.0); // V1 ( 1, 0, 0)
		 glVertex3f( 1.0f, 1.0f, 0.0); // V2 ( 1, 1, 0)
		 glVertex3f( 0.5f, 1.5f, 0.0); // V3 (0.5, 1.5, 0)
 		glVertex3f( 0.0, 1.0f, 0.0); // V4 ( 0, 1, 0)
	glEnd();

	glPushMatrix();
	glTranslatef(1.5, 2.0, 0.0);
	glRotatef(90.0, 0.0, 0.0, 1.0);
	glScalef(0.5, 0.5, 0.5);

	glBegin(GL_POLYGON);
		 glVertex3f( 0.0, 0.0, 0.0); // V0 ( 0, 0, 0)
		 glVertex3f( 1.0f, 0.0, 0.0); // V1 ( 1, 0, 0)
 		glVertex3f( 1.0f, 1.0f, 0.0); // V2 ( 1, 1, 0)
		 glVertex3f( 0.5f, 1.5f, 0.0); // V3 (0.5, 1.5, 0)
		 glVertex3f( 0.0, 1.0f, 0.0); // V4 ( 0, 1, 0)
	glEnd();
	glPopMatrix();
	glFlush();
	glutSwapBuffers();
}

void Init(void)
{
	glClearColor(0.0, 0.0, 0.0, 0.0);
}

void Resize(int width, int height)
{
	glViewport(0, 0, width, height);
	glMatrixMode(GL_PROJECTION);
	glLoadIdentity();
	gluPerspective(60.0, width/height, 0.1, 1000.0);
	glMatrixMode(GL_MODELVIEW);
	glLoadIdentity();
}

int main(int argc, char **argv)
{
	glutInit(&argc, argv);
	glutInitDisplayMode(GLUT_DOUBLE | GLUT_RGB);
	glutInitWindowSize(400, 400);
	glutInitWindowPosition(200, 200);
	glutCreateWindow("Polygon in OpenGL");
	 Init();
	glutDisplayFunc(Display);
	glutReshapeFunc(Resize);
	glutMainLoop();
	 return 0;
}


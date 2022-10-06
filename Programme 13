#include <windows.h>
#include <GL/glut.h>

void initGL() {

   glClearColor(0.0, 0.0, 0.0, 1.0);
}

void display() {
   glClear(GL_COLOR_BUFFER_BIT);

   glBegin(GL_TRIANGLES);
      glColor3f(0.0, 0.0, 1.0);
      glVertex2f(-0.3, -0.2);
      glVertex2f( 0.3, -0.2);
      glVertex2f( 0.0,  0.3);
   glEnd();

   glTranslatef(0.2, -0.3, 0.0);
   glScalef(2.0, 2.0, 2.0);
      glBegin(GL_TRIANGLES);
      glColor3f(1.0, 0.0, 0.0);
      glVertex2f(-0.3, -0.2);
      glColor3f(0.0, 1.0, 0.0);
      glVertex2f( 0.3, -0.2);
      glColor3f(0.0, 0.0, 1.0);
      glVertex2f( 0.0,  0.3);
   glEnd();

   glFlush();
}


int main(int argc, char** argv) {
   glutInit(&argc, argv);
   glutInitWindowSize(640, 480);
   glutInitWindowPosition(50, 50);
   glutCreateWindow("Model Transform");
   glutDisplayFunc(display);

   initGL();
   glutMainLoop();
   return 0;
}

#include<GL/glu.h>
#include <GL/glut.h>

void MyInit()
{
   glClearColor(0,0,1,1);
   glColor3f(1,0,0);
}
void draw()
{
  glClear(GL_COLOR_BUFFER_BIT);
  glPointSize(5);

 glBegin(GL_POLYGON);
    glVertex2f(0.0,0.6);
    glVertex2f(0.8,-0.6);
    glVertex2f(-.8,-0.6);
glEnd();

  glFlush();
}
int main(int c, char *v[])
{
    glutInit(&c,v);
    glutInitWindowPosition(300,300);
    glutInitWindowSize(400,400);
    glutInitDisplayMode(GLUT_RGB | GLUT_SINGLE);
    glutCreateWindow("My first window");

    MyInit();
    glutDisplayFunc(draw);
    glutMainLoop();
    return 0;
}

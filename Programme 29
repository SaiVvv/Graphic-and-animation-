#include<windows.h>
#include<GL/glut.h>
#include<math.h>

void Ellipse() {
GLfloat xi, yi, theta = 0;
GLfloat x_c = 0, y_c = 0, r_x = 0.8, r_y = 1.8;
int COUNT;
glClear(GL_COLOR_BUFFER_BIT);
for (COUNT = 1 ; COUNT <= 10000 ; COUNT++) {
theta = theta + 0.001;
xi = x_c + r_x*cos(theta);
yi = y_c + r_y*sin(theta);

glBegin(GL_POINTS);
glVertex2f(xi, yi);
glEnd();
}
glFlush();
}

void Initial() {
glClearColor(1.0, 0.5, 0.1, 0);
glColor3f(1,1,1);
glPointSize(5.0);
glMatrixMode(GL_PROJECTION);
glLoadIdentity();
gluOrtho2D(-2, +2, -2, +2);
}

int main(int c, char *v[])
{
glutInit(&c,v);
glutInitDisplayMode(GLUT_SINGLE | GLUT_RGB);
glutInitWindowSize(400, 400);
glutInitWindowPosition(0, 0);
glutCreateWindow("Draw Ellipse");
Initial();
glutDisplayFunc(Ellipse);
glutMainLoop();
return 0; 
}

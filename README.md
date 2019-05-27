# gsl-delphi
GSL For Delphi is a delphi header translation of GNU Scientific Library at https://www.gnu.org/software/gsl/ , lastest support version is 2.5+. Prebuilt 32bit windows dll also included in the bin folder.

# To use gsl to do linear regression

```pascal
procedure TFormMain.btnStatClick(Sender: TObject);
var
  I: Integer;
  X,Y:array [0..3] of Double;
  c0,c1, cov00, cov01, cov11, sumsq:double;
begin
  for I := 0 to 3 do
  begin
    X[I]:=I;
    Y[I]:=I*1.23+3.64;
  end;

  gsl_fit_linear(@X[0], 1, @Y[0], 1, 4, @c0,@c1,@cov00, @cov01, @cov11, @sumsq );


end;
```

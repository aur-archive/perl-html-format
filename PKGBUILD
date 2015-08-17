# Contributor: John D Jones III <j[nospace]n[nospace]b[nospace]e[nospace]k[nospace]1972 -_AT_- the domain name google offers a mail service at ending in dot com>
# Generator  : CPANPLUS::Dist::Arch 1.25

pkgname='perl-html-format'
pkgver='2.10'
pkgrel='1'
pkgdesc=""
arch=('any')
license=('PerlArtistic' 'GPL')
options=('!emptydirs')
depends=('perl>=5.008' 'perl-file-slurp' 'perl-font-afm' 'perl-html-tree')
makedepends=()
url='http://search.cpan.org/dist/HTML-Format'
source=('http://search.cpan.org/CPAN/authors/id/N/NI/NIGELM/HTML-Format-2.10.tar.gz')
md5sums=('34831ec506eaa8a7ad5da698224cf58d')
sha512sums=('a15a471fab17285704dbfb91b226d75d2bda0fbacbb5ce9259bc72fd4e7d5ba2129b5b4f133d68ebe3f03ddad0620e2e757f29bf4c7af819bf00333c2fad200c')
_distdir="HTML-Format-2.10"

build() {
  ( export PERL_MM_USE_DEFAULT=1 PERL5LIB=""                 \
      PERL_AUTOINSTALL=--skipdeps                            \
      PERL_MM_OPT="INSTALLDIRS=vendor DESTDIR='$pkgdir'"     \
      PERL_MB_OPT="--installdirs vendor --destdir '$pkgdir'" \
      MODULEBUILDRC=/dev/null

    cd "$srcdir/$_distdir"
    /usr/bin/perl Build.PL
    /usr/bin/perl Build
  )
}

check() {
  cd "$srcdir/$_distdir"
  ( export PERL_MM_USE_DEFAULT=1 PERL5LIB=""
    /usr/bin/perl Build test
  )
}

package() {
  cd "$srcdir/$_distdir"
  /usr/bin/perl Build install

  find "$pkgdir" -name .packlist -o -name perllocal.pod -delete
}

# Local Variables:
# mode: shell-script
# sh-basic-offset: 2
# End:
# vim:set ts=2 sw=2 et:

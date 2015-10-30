# sth-camouflage
Less mixins boilerplate
for quick building websites.

# install
    bower install Sth-Camouflage
    
#Usage
    @font-size-base: 14;
    // font-sizes for medium screen size
    @font-size-medium: 15;
    // font-size for small screen size
    @font-size-small: 16;
    // medium screen size
    @screen-medium: 1024px;
    // small screen size
    @screen-small: 640px;

    @import './sth-camouflage/_sth_base.less';
where @base-font-size is numeric value for pixel size of your fonts.

And that's it.

You can now use mixins like:

**.font-face(name, path);**

    .font-face('Hel, '../../assets/fonts');
returns fontface with font path and font name

    @font-face {
      font-family: 'Hel';
      src: url(../../assets/fonts/Hel/Hel.eot);
      src: url(../../assets/fonts/Hel/Hel.eot?#iefix) format('embedded-opentype'), url('../../assets/fonts/Hel/Hel.woff') format('woff'), url('../../assets/fonts/Hel/Hel.ttf') format('truetype');
      font-weight: normal;
      font-style: normal;
    }
**.for(array) .-each(name)**

    @fonts: 'Test', 'Abc';
    .for(@fonts);
        .-each(@name) {
            .test {
                font-family: @name;
            }
    }
returns:

    .test { font-family: Test}
    .test { font-family: Abc}

**.text-center**

    .test {
        .text-center;
    }

returns

    .test {
        text-align: center;
    }

// more info will be provided soon.

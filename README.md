Download Link: https://assignmentchef.com/product/solved-adipvc-assignment1
<br>
Read    the  colour  image  “Church.jpg”,  convert            it          to         gray     level    image  and      perform           the       following     operations.      Respective       marks  for       your     implementations are       shown  with     the       tasks    assigned    here.

<ul>

 <li>For reading            and      conversion       to             —</li>

 <li>On the       original            gray     image:             Add      random           noise    (Gaussian        noise    of       standard          deviation         5)         to                  Then    perform           denoising         by       performing      wavelet           analysis,          setting the       coefficients     below  a          threshold       value   (to        be        provided          by        the       user),   and      then     applying          wavelet       synthesis          on        the       images.           Apply   Le        Gall      5/3       wavelet           filters       (separable       in         2D)      for       this      purpose.          The      coefficients     of         these       filters   (in        1D)                  are       provided          in         the       Table   below.</li>

</ul>




<table width="559">

 <tbody>

  <tr>

   <td width="72"> </td>

   <td colspan="2" width="235">Analysis           Filter    Bank</td>

   <td colspan="2" width="252">Synthesis         Filter    Bank</td>

  </tr>

  <tr>

   <td width="72">n</td>

   <td width="117">Low-pass           filter</td>

   <td width="117">High    pass           filter</td>

   <td width="129">Low-pass            filter</td>

   <td width="123">High     pass            filter</td>

  </tr>

  <tr>

   <td width="72">0</td>

   <td width="117">3/4</td>

   <td width="117">1</td>

   <td width="129">1</td>

   <td width="123">3/4</td>

  </tr>

  <tr>

   <td width="72">±1</td>

   <td width="117">1/4</td>

   <td width="117">-1/2</td>

   <td width="129">1/2</td>

   <td width="123">1/4</td>

  </tr>

  <tr>

   <td width="72">±2</td>

   <td width="117">-1/8 </td>

   <td width="117"> </td>

   <td width="129"> </td>

   <td width="123">-1/8</td>

  </tr>

 </tbody>

</table>




For       applying          these   filters,  you      need    to         convolve          row      wise     and      column wise     with     1-D      filter    responses        for       Low-Low          (LL),     Low-High         (LH),    High-Low (HL)     and      High-High        (HH)     bands.  After    applying                      analysis           filters,  downsample filtered images by        half      in         both     directions.       Before applying          synthesis          filters upsample        them    by        the       factor  of         two      in         both     the       directions.       Summation of         responses        from    synthesis          filter    will      provide            the       reconstructed  image. For details refer    to         Fig.      3.1       of         the       attached          document        on        tutorial            of wavelet           transforms.




Also      apply   median            filtering           and      Gaussian          filtering           (of        standard deviation         4)         for       denoising.        Display the       original,           noisy,   and      all        filtered images.           Compute         the       PSNR    of         the       noisy    and      filtered images w.r.t.    the original            image  in         each    case.    –          Analysis           (10),     downsampling (5),       thresholding (10),     upsampling     (5),       Synthesis         (10),     Gaussian          filtering           (5),       Median filtering           (5),       Computing      PSNRs  (5),       Display (5)        =




<ul>

 <li>On the       original            gray     image: Apply   LoG      (Laplacian       of         Gaussian)        operator       of         standard          deviation         5,         and      find      edge    pixels   by        computing       its       zero             Display both     LOG     image  and      its        zero-crossings.            —       4+4+2=10</li>

 <li>On the       original            colour  image:             Apply   mean   shift     algorithm        for       segmenting       it          in         the       RGB     color      For       reference        please  consult the       attached       paper   .           —          15</li>

</ul>

Implement Harris corner detector          on        the       gray     image  and      display the       detected                  –







Bonus:              If          all        the       modules          are       implemented  and      the       results are shown  for       each    of         them.   —







You      may     implement      your     programs        in                     C++-OpenCV/MATLAB/          Python with     necessary        user’s   interfaces        and      visualization    of         your     results and      input.

Please  provide            a          documentation            for       compiling        and      running            the programs        in         a          README          file.      The      whole  project should  be        submitted        in a          single   tar       or         zip        file.



---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: AA7BD103-5C91-4E3B-9E46-2CAEDA5BA615
online version: ''
schema: 2.0.0
ms.openlocfilehash: d8f5643756cfad93399664298378e97264dedc2f
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/08/2020
ms.locfileid: "94007604"
---
# <span data-ttu-id="ee9ad-101">New-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="ee9ad-101">New-WAPackVM</span></span>

## <span data-ttu-id="ee9ad-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ee9ad-102">SYNOPSIS</span></span>
<span data-ttu-id="ee9ad-103">Erstellt einen virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="ee9ad-103">Creates a virtual machine.</span></span>

## <span data-ttu-id="ee9ad-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ee9ad-104">SYNTAX</span></span>

### <span data-ttu-id="ee9ad-105">CreateVMFromTemplate (Standard)</span><span class="sxs-lookup"><span data-stu-id="ee9ad-105">CreateVMFromTemplate (Default)</span></span>
```
New-WAPackVM -Name <String> -Template <VMTemplate> -VMCredential <PSCredential> [-VNet <VMNetwork>]
 [-ProductKey <String>] [-Windows] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="ee9ad-106">CreateLinuxVMFromTemplate</span><span class="sxs-lookup"><span data-stu-id="ee9ad-106">CreateLinuxVMFromTemplate</span></span>
```
New-WAPackVM -Name <String> -Template <VMTemplate> -VMCredential <PSCredential> [-VNet <VMNetwork>] [-Linux]
 [-AdministratorSSHKey <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="ee9ad-107">CreateVMFromOSDisk</span><span class="sxs-lookup"><span data-stu-id="ee9ad-107">CreateVMFromOSDisk</span></span>
```
New-WAPackVM -Name <String> [-VNet <VMNetwork>] -OSDisk <VirtualHardDisk> -VMSizeProfile <HardwareProfile>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ee9ad-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ee9ad-108">DESCRIPTION</span></span>
<span data-ttu-id="ee9ad-109">Diese Themen sind veraltet und werden in Zukunft entfernt.</span><span class="sxs-lookup"><span data-stu-id="ee9ad-109">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="ee9ad-110">In diesem Thema wird das Cmdlet in der Version 0.8.1 des Microsoft Azure PowerShell-Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="ee9ad-110">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="ee9ad-111">Wenn Sie die Version des verwendeten Moduls ermitteln möchten, geben Sie aus der Azure PowerShell-Konsole ein `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="ee9ad-111">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="ee9ad-112">Das Cmdlet **New-WAPackVM** erstellt einen virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="ee9ad-112">The **New-WAPackVM** cmdlet creates a virtual machine.</span></span>

## <span data-ttu-id="ee9ad-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ee9ad-113">EXAMPLES</span></span>

### <span data-ttu-id="ee9ad-114">Beispiel 1: Erstellen eines virtuellen Computers für das Windows-Betriebssystem mithilfe einer Vorlage</span><span class="sxs-lookup"><span data-stu-id="ee9ad-114">Example 1: Create a virtual machine for the Windows operating system by using a template</span></span>
```
PS C:\> $Credentials = Get-Credential PS C:\> $Template = Get-WAPackVMTemplate -Name "ContosoTemplate04"PS C:\> New-WAPackVM -Name "ContosoV023" -Template $Template -VMCredential $Credentials -Windows
```

<span data-ttu-id="ee9ad-115">Der erste Befehl erstellt ein **PSCredential** -Objekt und speichert es dann in der $Credentials-Variablen.</span><span class="sxs-lookup"><span data-stu-id="ee9ad-115">The first command creates a **PSCredential** object, and then stores it in the $Credentials variable.</span></span>
<span data-ttu-id="ee9ad-116">Das Cmdlet fordert Sie zur Eingabe eines Kontos und eines Kennworts auf.</span><span class="sxs-lookup"><span data-stu-id="ee9ad-116">The cmdlet prompts you for an account and password.</span></span>
<span data-ttu-id="ee9ad-117">Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="ee9ad-117">For more information, type `Get-Help Get-Credential`.</span></span>

<span data-ttu-id="ee9ad-118">Der zweite Befehl ruft die Vorlage für den virtuellen Computer mit dem Namen ContosoTemplate04 mit dem Cmdlet **Get-WAPackVMTemplate** ab und speichert Sie dann in der $Template-Variablen.</span><span class="sxs-lookup"><span data-stu-id="ee9ad-118">The second command gets the virtual machine template named ContosoTemplate04 by using the **Get-WAPackVMTemplate** cmdlet, and then stores it in the $Template variable.</span></span>

<span data-ttu-id="ee9ad-119">Der endgültige Befehl erstellt einen virtuellen Computer mit dem Namen ContosoV023, basierend auf der Vorlage, die in der $Template-Variablen gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="ee9ad-119">The final command creates a virtual machine named ContosoV023, based on the template stored in the $Template variable.</span></span>
<span data-ttu-id="ee9ad-120">Der Befehl gibt den *Windows* -Parameter an, und daher muss auf dem virtuellen Computer eine Version des Windows-Betriebssystems ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="ee9ad-120">The command specifies the *Windows* parameter, and, therefore, the virtual machine must run a version of the Windows operating system.</span></span>

### <span data-ttu-id="ee9ad-121">Beispiel 2: Erstellen eines virtuellen Computers für das Linux-Betriebssystem mithilfe einer Vorlage</span><span class="sxs-lookup"><span data-stu-id="ee9ad-121">Example 2: Create a virtual machine for the Linux operating system by using a template</span></span>
```
PS C:\> $Credentials = Get-Credential
PS C:\> $Template = Get-WAPackVMTemplate -Name "ContosoTemplate19"
PS C:\> New-WAPackVM -Linux -Name "ContosoV028" -Template $Template -VMCredential $Credentials
```

<span data-ttu-id="ee9ad-122">Der erste Befehl erstellt ein **PSCredential** -Objekt und speichert es dann in der $Credentials-Variablen.</span><span class="sxs-lookup"><span data-stu-id="ee9ad-122">The first command creates a **PSCredential** object, and then stores it in the $Credentials variable.</span></span>

<span data-ttu-id="ee9ad-123">Der zweite Befehl ruft die Vorlage für den virtuellen Computer mit dem Namen ContosoTemplate19 mit dem Cmdlet **Get-WAPackVMTemplate** ab und speichert Sie dann in der $Template-Variablen.</span><span class="sxs-lookup"><span data-stu-id="ee9ad-123">The second command gets the virtual machine template named ContosoTemplate19 by using the **Get-WAPackVMTemplate** cmdlet, and then stores it in the $Template variable.</span></span>

<span data-ttu-id="ee9ad-124">Der endgültige Befehl erstellt einen virtuellen Computer mit dem Namen ContosoV028, basierend auf der Vorlage, die in der $Template-Variablen gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="ee9ad-124">The final command creates a virtual machine named ContosoV028, based on the template stored in the $Template variable.</span></span>
<span data-ttu-id="ee9ad-125">Der Befehl gibt den *Linux* -Parameter an, und daher muss auf dem virtuellen Computer eine Version des Linux-Betriebssystems ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="ee9ad-125">The command specifies the *Linux* parameter, and, therefore, the virtual machine must run a version of the Linux operating system.</span></span>

### <span data-ttu-id="ee9ad-126">Beispiel 3: Erstellen eines virtuellen Computers aus einem Betriebssystemdatenträger und einem Größen Profil</span><span class="sxs-lookup"><span data-stu-id="ee9ad-126">Example 3: Create a virtual machine from an operating system disk and size profile</span></span>
```
PS C:\> $OSDisk = Get-WAPackVMOSDisk -Name "ContosoDiskOS"
PS C:\> $SizeProfile = Get-WAPackVMSizeProfile -Name "MediumSizeVM"
PS C:\> New-WAPackVM -Name "ContosoV073" -OSDisk $OSDisk -VMSizeProfile $SizeProfile
```

<span data-ttu-id="ee9ad-127">Der erste Befehl ruft mit dem Cmdlet **Get-WAPackVMOSDisk** einen Betriebssystemdatenträger mit dem Namen ContosoDiskOS ab und speichert ihn dann in der $OSDisk Variablen.</span><span class="sxs-lookup"><span data-stu-id="ee9ad-127">The first command gets an operating system disk named ContosoDiskOS by using the **Get-WAPackVMOSDisk** cmdlet, and then stores it in the $OSDisk variable.</span></span>

<span data-ttu-id="ee9ad-128">Der zweite Befehl ruft das size-Profil mit dem Namen MediumSizeVM mit dem Cmdlet **Get-WAPackVMSizeProfile** ab und speichert es dann in der $SizeProfile-Variablen.</span><span class="sxs-lookup"><span data-stu-id="ee9ad-128">The second command gets the size profile named MediumSizeVM by using the **Get-WAPackVMSizeProfile** cmdlet, and then stores it in the $SizeProfile variable.</span></span>

<span data-ttu-id="ee9ad-129">Der endgültige Befehl erstellt einen virtuellen Computer mit dem Namen ContosoV073 aus dem in $OSDisk gespeicherten Betriebssystemdatenträger und dem in $SizeProfile gespeicherten Größen Profil.</span><span class="sxs-lookup"><span data-stu-id="ee9ad-129">The final command creates a virtual machine named ContosoV073 from the operating system disk stored in $OSDisk and the size profile stored in $SizeProfile.</span></span>

## <span data-ttu-id="ee9ad-130">Parameter</span><span class="sxs-lookup"><span data-stu-id="ee9ad-130">PARAMETERS</span></span>

### <span data-ttu-id="ee9ad-131">-AdministratorSSHKey</span><span class="sxs-lookup"><span data-stu-id="ee9ad-131">-AdministratorSSHKey</span></span>
<span data-ttu-id="ee9ad-132">Gibt den Secure Shell (SSH)-Schlüssel für das Administrator Konto an.</span><span class="sxs-lookup"><span data-stu-id="ee9ad-132">Specifies the Secure Shell (SSH) key for the Administrator account.</span></span>

```yaml
Type: String
Parameter Sets: CreateLinuxVMFromTemplate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee9ad-133">-Linux</span><span class="sxs-lookup"><span data-stu-id="ee9ad-133">-Linux</span></span>
<span data-ttu-id="ee9ad-134">Gibt an, dass das Cmdlet einen virtuellen Computer zum Ausführen des Linux-Betriebssystems erstellt.</span><span class="sxs-lookup"><span data-stu-id="ee9ad-134">Indicates that the cmdlet creates a virtual machine to run the Linux operating system.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: CreateLinuxVMFromTemplate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee9ad-135">-Name</span><span class="sxs-lookup"><span data-stu-id="ee9ad-135">-Name</span></span>
<span data-ttu-id="ee9ad-136">Gibt einen Namen für den virtuellen Computer an.</span><span class="sxs-lookup"><span data-stu-id="ee9ad-136">Specifies a name for the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee9ad-137">-OSDisk</span><span class="sxs-lookup"><span data-stu-id="ee9ad-137">-OSDisk</span></span>
<span data-ttu-id="ee9ad-138">Gibt einen Betriebssystemdatenträger als **VirtualHardDisk** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="ee9ad-138">Specifies an operating system disk as a **VirtualHardDisk** object.</span></span>
<span data-ttu-id="ee9ad-139">Um einen Betriebssystemdatenträger zu erhalten, verwenden Sie das Cmdlet **Get-WAPackVMOSDisk** .</span><span class="sxs-lookup"><span data-stu-id="ee9ad-139">To obtain an operating system disk, use the **Get-WAPackVMOSDisk** cmdlet.</span></span>

```yaml
Type: VirtualHardDisk
Parameter Sets: CreateVMFromOSDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee9ad-140">-ProductKey</span><span class="sxs-lookup"><span data-stu-id="ee9ad-140">-ProductKey</span></span>
<span data-ttu-id="ee9ad-141">Gibt einen Product Key an.</span><span class="sxs-lookup"><span data-stu-id="ee9ad-141">Specifies a product key.</span></span>
<span data-ttu-id="ee9ad-142">Der Product Key ist eine 25-stellige Nummer, die die Produktlizenz kennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="ee9ad-142">The product key is a 25 digit number that identifies the product license.</span></span>
<span data-ttu-id="ee9ad-143">Verwenden Sie einen Product Key für ein Betriebssystem, das Sie auf einem virtuellen Computer oder einem Host installieren möchten.</span><span class="sxs-lookup"><span data-stu-id="ee9ad-143">Use a product key for an operating system that you plan to install on a virtual machine or host.</span></span>

```yaml
Type: String
Parameter Sets: CreateVMFromTemplate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee9ad-144">-Profil</span><span class="sxs-lookup"><span data-stu-id="ee9ad-144">-Profile</span></span>
<span data-ttu-id="ee9ad-145">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="ee9ad-145">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ee9ad-146">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="ee9ad-146">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee9ad-147">-Vorlage</span><span class="sxs-lookup"><span data-stu-id="ee9ad-147">-Template</span></span>
<span data-ttu-id="ee9ad-148">Gibt eine Vorlage an.</span><span class="sxs-lookup"><span data-stu-id="ee9ad-148">Specifies a template.</span></span>
<span data-ttu-id="ee9ad-149">Das Cmdlet erstellt einen virtuellen Computer basierend auf der von Ihnen angegebenen Vorlage.</span><span class="sxs-lookup"><span data-stu-id="ee9ad-149">The cmdlet creates a virtual machine based on the template that you specify.</span></span>
<span data-ttu-id="ee9ad-150">Verwenden Sie zum Abrufen eines Vorlagenobjekts das Get-WAPackVMTemplate-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee9ad-150">To obtain a template object, use the Get-WAPackVMTemplate cmdlet.</span></span>

```yaml
Type: VMTemplate
Parameter Sets: CreateVMFromTemplate, CreateLinuxVMFromTemplate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee9ad-151">-VMCredential</span><span class="sxs-lookup"><span data-stu-id="ee9ad-151">-VMCredential</span></span>
<span data-ttu-id="ee9ad-152">Gibt die Anmeldeinformationen für das lokale Administrator Konto an.</span><span class="sxs-lookup"><span data-stu-id="ee9ad-152">Specifies the credential for the local Administrator account.</span></span>
<span data-ttu-id="ee9ad-153">Verwenden Sie das Cmdlet **Get-Credential** , um ein **PSCredential** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="ee9ad-153">To obtain a **PSCredential** object, use the **Get-Credential** cmdlet.</span></span>
<span data-ttu-id="ee9ad-154">Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="ee9ad-154">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: PSCredential
Parameter Sets: CreateVMFromTemplate, CreateLinuxVMFromTemplate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee9ad-155">-VMSizeProfile</span><span class="sxs-lookup"><span data-stu-id="ee9ad-155">-VMSizeProfile</span></span>
<span data-ttu-id="ee9ad-156">Gibt ein Größen Profil für einen virtuellen Computer als **Hardwareprofile** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="ee9ad-156">Specifies a size profile for a virtual machine as a **HardwareProfile** object.</span></span>
<span data-ttu-id="ee9ad-157">Um ein Größen Profil zu erhalten, verwenden Sie das Cmdlet **Get-WAPackVMSizeProfile** .</span><span class="sxs-lookup"><span data-stu-id="ee9ad-157">To obtain a size profile, use the **Get-WAPackVMSizeProfile** cmdlet.</span></span>

```yaml
Type: HardwareProfile
Parameter Sets: CreateVMFromOSDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee9ad-158">-VNet</span><span class="sxs-lookup"><span data-stu-id="ee9ad-158">-VNet</span></span>
<span data-ttu-id="ee9ad-159">Gibt ein virtuelles Netzwerk an.</span><span class="sxs-lookup"><span data-stu-id="ee9ad-159">Specifies a virtual network.</span></span>
<span data-ttu-id="ee9ad-160">Das Cmdlet verbindet den virtuellen Computer mit dem von Ihnen angegebenen virtuellen Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="ee9ad-160">The cmdlet connects the virtual machine to the virtual network that you specify.</span></span>
<span data-ttu-id="ee9ad-161">Um ein virtuelles Netzwerk zu erhalten, verwenden Sie das Cmdlet **Get-WAPackVNet** .</span><span class="sxs-lookup"><span data-stu-id="ee9ad-161">To obtain a virtual network, use the **Get-WAPackVNet** cmdlet.</span></span>

```yaml
Type: VMNetwork
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee9ad-162">-Windows</span><span class="sxs-lookup"><span data-stu-id="ee9ad-162">-Windows</span></span>
<span data-ttu-id="ee9ad-163">Gibt an, dass das Cmdlet einen virtuellen Computer zum Ausführen des Windows-Betriebssystems erstellt.</span><span class="sxs-lookup"><span data-stu-id="ee9ad-163">Indicates that the cmdlet creates a virtual machine to run the Windows operating system.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: CreateVMFromTemplate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee9ad-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee9ad-164">CommonParameters</span></span>
<span data-ttu-id="ee9ad-165">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee9ad-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee9ad-166">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee9ad-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee9ad-167">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ee9ad-167">INPUTS</span></span>

## <span data-ttu-id="ee9ad-168">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ee9ad-168">OUTPUTS</span></span>

## <span data-ttu-id="ee9ad-169">Notizen</span><span class="sxs-lookup"><span data-stu-id="ee9ad-169">NOTES</span></span>

## <span data-ttu-id="ee9ad-170">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ee9ad-170">RELATED LINKS</span></span>

[<span data-ttu-id="ee9ad-171">Get-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="ee9ad-171">Get-WAPackVM</span></span>](./Get-WAPackVM.md)

[<span data-ttu-id="ee9ad-172">Remove-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="ee9ad-172">Remove-WAPackVM</span></span>](./Remove-WAPackVM.md)

[<span data-ttu-id="ee9ad-173">Neustart-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="ee9ad-173">Restart-WAPackVM</span></span>](./Restart-WAPackVM.md)

[<span data-ttu-id="ee9ad-174">Lebenslauf-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="ee9ad-174">Resume-WAPackVM</span></span>](./Resume-WAPackVM.md)

[<span data-ttu-id="ee9ad-175">Satz-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="ee9ad-175">Set-WAPackVM</span></span>](./Set-WAPackVM.md)

[<span data-ttu-id="ee9ad-176">Anfang-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="ee9ad-176">Start-WAPackVM</span></span>](./Start-WAPackVM.md)

[<span data-ttu-id="ee9ad-177">Stopp-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="ee9ad-177">Stop-WAPackVM</span></span>](./Stop-WAPackVM.md)

[<span data-ttu-id="ee9ad-178">Suspend-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="ee9ad-178">Suspend-WAPackVM</span></span>](./Suspend-WAPackVM.md)

[<span data-ttu-id="ee9ad-179">Get-WAPackVMSizeProfile</span><span class="sxs-lookup"><span data-stu-id="ee9ad-179">Get-WAPackVMSizeProfile</span></span>](./Get-WAPackVMSizeProfile.md)

[<span data-ttu-id="ee9ad-180">Get-WAPackVMTemplate</span><span class="sxs-lookup"><span data-stu-id="ee9ad-180">Get-WAPackVMTemplate</span></span>](./Get-WAPackVMTemplate.md)

[<span data-ttu-id="ee9ad-181">Get-WAPackVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="ee9ad-181">Get-WAPackVMOSDisk</span></span>](./Get-WAPackVMOSDisk.md)



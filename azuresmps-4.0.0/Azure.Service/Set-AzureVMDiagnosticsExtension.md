---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: A05B39BF-87EB-471E-9FCD-F7807CB46B4D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1aa7cff6d655bf33fa1a317516fda20237f6fc14
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006244"
---
# <span data-ttu-id="8a231-101">Set-AzureVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="8a231-101">Set-AzureVMDiagnosticsExtension</span></span>

## <span data-ttu-id="8a231-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8a231-102">SYNOPSIS</span></span>
<span data-ttu-id="8a231-103">Konfiguriert die Azure Diagnostics-Erweiterung auf einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="8a231-103">Configures the Azure Diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="8a231-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8a231-104">SYNTAX</span></span>

### <span data-ttu-id="8a231-105">SetDiagnosticsExtension (Standard)</span><span class="sxs-lookup"><span data-stu-id="8a231-105">SetDiagnosticsExtension (Default)</span></span>
```
Set-AzureVMDiagnosticsExtension [-DiagnosticsConfigurationPath] <String> [[-StorageAccountName] <String>]
 [[-StorageAccountKey] <String>] [[-StorageAccountEndpoint] <String>] [[-StorageContext] <AzureStorageContext>]
 [[-Version] <String>] [-Disable] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="8a231-106">SetDiagnosticsWithReferenceExtension</span><span class="sxs-lookup"><span data-stu-id="8a231-106">SetDiagnosticsWithReferenceExtension</span></span>
```
Set-AzureVMDiagnosticsExtension [-DiagnosticsConfigurationPath] <String> [[-StorageAccountName] <String>]
 [[-StorageAccountKey] <String>] [[-StorageAccountEndpoint] <String>] [[-StorageContext] <AzureStorageContext>]
 [[-Version] <String>] [-Disable] [[-ReferenceName] <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="8a231-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8a231-107">DESCRIPTION</span></span>
<span data-ttu-id="8a231-108">Mit dem Cmdlet " **festlegen-AzureVMDiagnosticsExtension** " wird die Microsoft Azure Diagnostics-Erweiterung auf einem virtuellen Computer konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="8a231-108">The **Set-AzureVMDiagnosticsExtension** cmdlet configures the Microsoft Azure Diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="8a231-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8a231-109">EXAMPLES</span></span>

### <span data-ttu-id="8a231-110">Beispiel 1: Erstellen eines virtuellen Computers mit angewendeter Azure Diagnostics-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="8a231-110">Example 1: Create a virtual machine with Azure Diagnostics extension applied</span></span>
```
PS C:\> $VM = New-AzureVMConfig -Name $VM -InstanceSize Small -ImageName $VMImage
PS C:\> $VM = Add-AzureProvisioningConfig -VM $VM -AdminUsername $Username -Password $Password -Windows
PS C:\> $VM = Set-AzureVMDiagnosticsExtension -DiagnosticsConfigurationPath $Config_Path -Version "1.*" -VM $VM -StorageContext $Storage_Context
PS C:\> New-AzureVM -Location $Location -ServiceName $Service_Name -VM $VM
```

<span data-ttu-id="8a231-111">Mit diesen Befehlen wird die Azure Diagnostics-Erweiterung auf einem virtuellen Computer aktiviert.</span><span class="sxs-lookup"><span data-stu-id="8a231-111">These commands enable the Azure Diagnostics extension on a virtual machine.</span></span>

### <span data-ttu-id="8a231-112">Beispiel 2: Aktivieren einer Azure Diagnostics-Erweiterung auf einem vorhandenen virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="8a231-112">Example 2: Enable an Azure Diagnostics extension on an existing virtual machine</span></span>
```
PS C:\> $VM = Get-AzureVM -ServiceName $Service_Name -Name $VM_Name
PS C:\> $VM_Update = Set-AzureVMDiagnosticsExtension -DiagnosticsConfigurationPath $Config_Path -Version "1.*" -VM $VM -StorageContext $Storage_Context
PS C:\> Update-AzureVM -ServiceName $Service_Name -Name $VM_Name -VM $VM_Update.VM
```

<span data-ttu-id="8a231-113">Der erste Befehl verwendet das Cmdlet " **Get-AzureVM** ", um einen virtuellen Computer abzurufen.</span><span class="sxs-lookup"><span data-stu-id="8a231-113">The first command uses the **Get-AzureVM** cmdlet to get a virtual machine.</span></span>

<span data-ttu-id="8a231-114">Der zweite Befehl verwendet das Cmdlet " **AzureVMDiagnosticsExtension** ", um die Konfiguration des virtuellen Computers so zu aktualisieren, dass die Azure Diagnostics-Erweiterung einbezogen wird.</span><span class="sxs-lookup"><span data-stu-id="8a231-114">The second command uses the **Set-AzureVMDiagnosticsExtension** cmdlet to update the virtual machine configuration to include the Azure Diagnostics extension.</span></span>

<span data-ttu-id="8a231-115">Der endgültige Befehl wendet die aktualisierte Konfiguration auf den virtuellen Computer an.</span><span class="sxs-lookup"><span data-stu-id="8a231-115">The final command applies the updated configuration to the virtual machine.</span></span>

## <span data-ttu-id="8a231-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="8a231-116">PARAMETERS</span></span>

### <span data-ttu-id="8a231-117">-DiagnosticsConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="8a231-117">-DiagnosticsConfigurationPath</span></span>
<span data-ttu-id="8a231-118">Gibt einen Pfad für die Diagnose Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="8a231-118">Specifies a path for the diagnostics configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a231-119">-Deaktivieren Sie</span><span class="sxs-lookup"><span data-stu-id="8a231-119">-Disable</span></span>
<span data-ttu-id="8a231-120">Gibt an, dass dieses Cmdlet die Diagnose Erweiterung auf dem virtuellen Computer deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="8a231-120">Indicates that this cmdlet disables the diagnostics extension on the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a231-121">-Information</span><span class="sxs-lookup"><span data-stu-id="8a231-121">-InformationAction</span></span>
<span data-ttu-id="8a231-122">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="8a231-122">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="8a231-123">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="8a231-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8a231-124">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="8a231-124">Continue</span></span>
- <span data-ttu-id="8a231-125">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="8a231-125">Ignore</span></span>
- <span data-ttu-id="8a231-126">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="8a231-126">Inquire</span></span>
- <span data-ttu-id="8a231-127">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="8a231-127">SilentlyContinue</span></span>
- <span data-ttu-id="8a231-128">Beenden</span><span class="sxs-lookup"><span data-stu-id="8a231-128">Stop</span></span>
- <span data-ttu-id="8a231-129">Anhalten</span><span class="sxs-lookup"><span data-stu-id="8a231-129">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a231-130">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="8a231-130">-InformationVariable</span></span>
<span data-ttu-id="8a231-131">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="8a231-131">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a231-132">-Profil</span><span class="sxs-lookup"><span data-stu-id="8a231-132">-Profile</span></span>
<span data-ttu-id="8a231-133">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="8a231-133">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8a231-134">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="8a231-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8a231-135">-ReferenceName</span><span class="sxs-lookup"><span data-stu-id="8a231-135">-ReferenceName</span></span>
<span data-ttu-id="8a231-136">Gibt den Verweisnamen für die Diagnose Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="8a231-136">Specifies the reference name for the diagnostics extension.</span></span>

```yaml
Type: String
Parameter Sets: SetDiagnosticsWithReferenceExtension
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a231-137">-StorageAccountEndpoint</span><span class="sxs-lookup"><span data-stu-id="8a231-137">-StorageAccountEndpoint</span></span>
<span data-ttu-id="8a231-138">Gibt einen Speicherkonto Endpunkt an.</span><span class="sxs-lookup"><span data-stu-id="8a231-138">Specifies a storage account endpoint.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a231-139">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="8a231-139">-StorageAccountKey</span></span>
<span data-ttu-id="8a231-140">Gibt einen speicherkontoschlüssel an.</span><span class="sxs-lookup"><span data-stu-id="8a231-140">Specifies a storage account key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a231-141">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="8a231-141">-StorageAccountName</span></span>
<span data-ttu-id="8a231-142">Gibt den Namen eines speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="8a231-142">Specifies a storage account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a231-143">-Storagecontext</span><span class="sxs-lookup"><span data-stu-id="8a231-143">-StorageContext</span></span>
<span data-ttu-id="8a231-144">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="8a231-144">Specifies an Azure storage context.</span></span>

```yaml
Type: AzureStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a231-145">-Version</span><span class="sxs-lookup"><span data-stu-id="8a231-145">-Version</span></span>
<span data-ttu-id="8a231-146">Gibt die Erweiterungsversion als Zeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="8a231-146">Specifies the extension version as a string.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a231-147">-VM</span><span class="sxs-lookup"><span data-stu-id="8a231-147">-VM</span></span>
<span data-ttu-id="8a231-148">Gibt das Objekt des beständigen virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="8a231-148">Specifies the persistent virtual machine object.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8a231-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a231-149">CommonParameters</span></span>
<span data-ttu-id="8a231-150">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a231-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a231-151">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a231-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a231-152">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8a231-152">INPUTS</span></span>

## <span data-ttu-id="8a231-153">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8a231-153">OUTPUTS</span></span>

## <span data-ttu-id="8a231-154">Notizen</span><span class="sxs-lookup"><span data-stu-id="8a231-154">NOTES</span></span>

## <span data-ttu-id="8a231-155">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8a231-155">RELATED LINKS</span></span>

[<span data-ttu-id="8a231-156">Get-AzureVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="8a231-156">Get-AzureVMDiagnosticsExtension</span></span>](./Get-AzureVMDiagnosticsExtension.md)

[<span data-ttu-id="8a231-157">Remove-AzureVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="8a231-157">Remove-AzureVMDiagnosticsExtension</span></span>](./Remove-AzureVMDiagnosticsExtension.md)

[<span data-ttu-id="8a231-158">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="8a231-158">Update-AzureVM</span></span>](./Update-AzureVM.md)



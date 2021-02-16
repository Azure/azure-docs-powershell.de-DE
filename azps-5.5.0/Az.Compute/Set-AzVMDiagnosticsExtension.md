---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 13ED884A-6224-4BD4-9F12-F896932F7842
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDiagnosticsExtension.md
ms.openlocfilehash: 5705d899f06d4a834b8864ec2a66c268e1c99c84
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100166404"
---
# <span data-ttu-id="ea265-101">Set-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="ea265-101">Set-AzVMDiagnosticsExtension</span></span>

## <span data-ttu-id="ea265-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea265-102">SYNOPSIS</span></span>
<span data-ttu-id="ea265-103">Konfiguriert die Azure-Diagnoseerweiterung auf einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="ea265-103">Configures the Azure diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="ea265-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ea265-104">SYNTAX</span></span>

```
Set-AzVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String>
 [-DiagnosticsConfigurationPath] <String> [[-StorageAccountName] <String>] [[-StorageAccountKey] <String>]
 [[-StorageAccountEndpoint] <String>] [[-StorageContext] <IStorageContext>] [[-Location] <String>]
 [[-Name] <String>] [[-TypeHandlerVersion] <String>] [[-AutoUpgradeMinorVersion] <Boolean>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ea265-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ea265-105">DESCRIPTION</span></span>
<span data-ttu-id="ea265-106">Das **Cmdlet Set-AzVMDiagnosticsExtension** konfiguriert die Azure-Diagnoseerweiterung auf einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="ea265-106">The **Set-AzVMDiagnosticsExtension** cmdlet configures the Azure diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="ea265-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ea265-107">EXAMPLES</span></span>

### <span data-ttu-id="ea265-108">Beispiel 1: Aktivieren der Diagnose mithilfe eines Speicherkontos, das in einer Diagnosekonfigurationsdatei angegeben ist</span><span class="sxs-lookup"><span data-stu-id="ea265-108">Example 1: Enable diagnostics using a storage account specified in a diagnostics configuration file</span></span>
```
PS C:\> Set-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup01" -VMName "VirtualMachine02" -DiagnosticsConfigurationPath "diagnostics_publicconfig.xml"
```

<span data-ttu-id="ea265-109">Dieser Befehl verwendet eine Diagnosekonfigurationsdatei, um die Diagnose zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="ea265-109">This command uses a diagnostics configuration file to enable diagnostics.</span></span>
<span data-ttu-id="ea265-110">Die Dateidateidiagnostics_publicconfig.xml enthält die öffentliche XML-Konfiguration für die Diagnoseerweiterung, einschließlich des Namens des Speicherkontos, an das Diagnosedaten gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="ea265-110">The file diagnostics_publicconfig.xml contains the public XML configuration for the diagnostics extension including the name of the storage account to which diagnostics data will be sent.</span></span>
<span data-ttu-id="ea265-111">Das Speicherkonto für die Diagnose muss im selben Abonnement wie der virtuelle Computer enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="ea265-111">The diagnostics storage account must be in the same subscription as the virtual machine.</span></span>

### <span data-ttu-id="ea265-112">Beispiel 2: Aktivieren der Diagnose mithilfe eines Speicherkontonamens</span><span class="sxs-lookup"><span data-stu-id="ea265-112">Example 2: Enable diagnostics using a storage account name</span></span>
```
PS C:\> Set-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup1" -VMName "VirtualMachine2" -DiagnosticsConfigurationPath diagnostics_publicconfig.xml -StorageAccountName "MyStorageAccount"
```

<span data-ttu-id="ea265-113">Dieser Befehl verwendet den Namen des Speicherkontos, um die Diagnose zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="ea265-113">This command uses the storage account name to enable diagnostics.</span></span>
<span data-ttu-id="ea265-114">Wenn in der Diagnosekonfiguration kein Speicherkontoname angegeben wird oder Sie den in der Konfigurationsdatei angegebenen Namen des Diagnosespeicherkontos außer Kraft setzen möchten, verwenden Sie den *Parameter "StorageAccountName".*</span><span class="sxs-lookup"><span data-stu-id="ea265-114">If the diagnostics configuration does not specify a storage account name or if you want to override the diagnostics storage account name specified in the configuration file, use the *StorageAccountName* parameter.</span></span>
<span data-ttu-id="ea265-115">Das Speicherkonto für die Diagnose muss im selben Abonnement wie der virtuelle Computer enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="ea265-115">The diagnostics storage account must be in the same subscription as the virtual machine.</span></span>

### <span data-ttu-id="ea265-116">Beispiel 3: Aktivieren der Diagnose mithilfe von Name und Schlüssel des Speicherkontos</span><span class="sxs-lookup"><span data-stu-id="ea265-116">Example 3: Enable diagnostics using storage account name and key</span></span>
```
PS C:\> Set-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup01" -VMName "VirtualMachine02" -DiagnosticsConfigurationPath "diagnostics_publicconfig.xml" -StorageAccountName "MyStorageAccount" -StorageAccountKey $storage_key
```

<span data-ttu-id="ea265-117">Dieser Befehl verwendet den Namen und Schlüssel des Speicherkontos, um die Diagnose zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="ea265-117">This command uses the storage account name and key to enable diagnostics.</span></span>
<span data-ttu-id="ea265-118">Wenn das Speicherkonto für die Diagnose in einem anderen Abonnement als der virtuelle Computer enthalten ist, aktivieren Sie das Senden von Diagnosedaten an dieses Speicherkonto, indem Sie dessen Namen und Schlüssel explizit angeben.</span><span class="sxs-lookup"><span data-stu-id="ea265-118">If the diagnostics storage account is in a different subscription than the virtual machine then enable sending diagnostics data to that storage account by explicitly specifying its name and key.</span></span>

## <span data-ttu-id="ea265-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ea265-119">PARAMETERS</span></span>

### <span data-ttu-id="ea265-120">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="ea265-120">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="ea265-121">Gibt an, ob dieses Cmdlet es dem Azure-Gast-Agent erlaubt, die Erweiterung automatisch auf eine neuere Nebenversion zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="ea265-121">Indicates whether this cmdlet allows the Azure guest agent to automatically update the extension to a newer minor version.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea265-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea265-122">-DefaultProfile</span></span>
<span data-ttu-id="ea265-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ea265-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea265-124">-DiagnosticsConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="ea265-124">-DiagnosticsConfigurationPath</span></span>
<span data-ttu-id="ea265-125">Gibt den Pfad der Konfigurationsdatei an.</span><span class="sxs-lookup"><span data-stu-id="ea265-125">Specifies the path of the configuration file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea265-126">-Location</span><span class="sxs-lookup"><span data-stu-id="ea265-126">-Location</span></span>
<span data-ttu-id="ea265-127">Gibt den Speicherort des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="ea265-127">Specifies the location of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea265-128">-Name</span><span class="sxs-lookup"><span data-stu-id="ea265-128">-Name</span></span>
<span data-ttu-id="ea265-129">Gibt den Namen einer Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="ea265-129">Specifies the name of an extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea265-130">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ea265-130">-NoWait</span></span>
<span data-ttu-id="ea265-131">Der Vorgang wird gestartet und unmittelbar vor Abschluss des Vorgangs beendet.</span><span class="sxs-lookup"><span data-stu-id="ea265-131">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="ea265-132">Verwenden Sie einen anderen Mechanismus, um festzustellen, ob der Vorgang erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="ea265-132">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea265-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea265-133">-ResourceGroupName</span></span>
<span data-ttu-id="ea265-134">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="ea265-134">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea265-135">-StorageAccountEndpoint</span><span class="sxs-lookup"><span data-stu-id="ea265-135">-StorageAccountEndpoint</span></span>
<span data-ttu-id="ea265-136">Gibt den Endpunkt des Speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="ea265-136">Specifies the storage account endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea265-137">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="ea265-137">-StorageAccountKey</span></span>
<span data-ttu-id="ea265-138">Gibt den Speicherkontoschlüssel an.</span><span class="sxs-lookup"><span data-stu-id="ea265-138">Specifies the storage account key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea265-139">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ea265-139">-StorageAccountName</span></span>
<span data-ttu-id="ea265-140">Gibt den Namen des Speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="ea265-140">Specifies the storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea265-141">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="ea265-141">-StorageContext</span></span>
<span data-ttu-id="ea265-142">Gibt den Azure -Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="ea265-142">Specifies the Azure storage context.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea265-143">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="ea265-143">-TypeHandlerVersion</span></span>
<span data-ttu-id="ea265-144">Gibt die Version der Erweiterung an, die für diesen virtuellen Computer verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ea265-144">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="ea265-145">Führen Sie zum Abrufen der Version das Get-AzVMExtensionImage cmdlet mit dem Wert "Microsoft.Compute" für den *Parameter "PublisherName"* und "VMAccessAgent" für den Parameter *"Type"* aus.</span><span class="sxs-lookup"><span data-stu-id="ea265-145">To obtain the version, run the Get-AzVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and VMAccessAgent for the *Type* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea265-146">-VMName</span><span class="sxs-lookup"><span data-stu-id="ea265-146">-VMName</span></span>
<span data-ttu-id="ea265-147">Gibt den Namen des virtuellen Computers an, auf dem dieses Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ea265-147">Specifies the name of the virtual machine on which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea265-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea265-148">CommonParameters</span></span>
<span data-ttu-id="ea265-149">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea265-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea265-150">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ea265-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea265-151">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ea265-151">INPUTS</span></span>

### <span data-ttu-id="ea265-152">System.String</span><span class="sxs-lookup"><span data-stu-id="ea265-152">System.String</span></span>

### <span data-ttu-id="ea265-153">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="ea265-153">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

### <span data-ttu-id="ea265-154">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ea265-154">System.Boolean</span></span>

## <span data-ttu-id="ea265-155">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ea265-155">OUTPUTS</span></span>

### <span data-ttu-id="ea265-156">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="ea265-156">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="ea265-157">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ea265-157">NOTES</span></span>

## <span data-ttu-id="ea265-158">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ea265-158">RELATED LINKS</span></span>

[<span data-ttu-id="ea265-159">Get-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="ea265-159">Get-AzVMDiagnosticsExtension</span></span>](./Get-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="ea265-160">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="ea265-160">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)

[<span data-ttu-id="ea265-161">Remove-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="ea265-161">Remove-AzVMDiagnosticsExtension</span></span>](./Remove-AzVMDiagnosticsExtension.md)



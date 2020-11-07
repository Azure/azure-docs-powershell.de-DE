---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 13ED884A-6224-4BD4-9F12-F896932F7842
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDiagnosticsExtension.md
ms.openlocfilehash: ed3215d6ae5b4e6386dc1ee9fce951f8b036d39d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651916"
---
# <span data-ttu-id="e01d6-101">Set-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="e01d6-101">Set-AzVMDiagnosticsExtension</span></span>

## <span data-ttu-id="e01d6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e01d6-102">SYNOPSIS</span></span>
<span data-ttu-id="e01d6-103">Konfiguriert die Azure Diagnostics-Erweiterung auf einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="e01d6-103">Configures the Azure diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="e01d6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e01d6-104">SYNTAX</span></span>

```
Set-AzVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String>
 [-DiagnosticsConfigurationPath] <String> [[-StorageAccountName] <String>] [[-StorageAccountKey] <String>]
 [[-StorageAccountEndpoint] <String>] [[-StorageContext] <IStorageContext>] [[-Location] <String>]
 [[-Name] <String>] [[-TypeHandlerVersion] <String>] [[-AutoUpgradeMinorVersion] <Boolean>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e01d6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e01d6-105">DESCRIPTION</span></span>
<span data-ttu-id="e01d6-106">Das Cmdlet " **Satz-AzVMDiagnosticsExtension** " konfiguriert die Azure Diagnostics-Erweiterung auf einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="e01d6-106">The **Set-AzVMDiagnosticsExtension** cmdlet configures the Azure diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="e01d6-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e01d6-107">EXAMPLES</span></span>

### <span data-ttu-id="e01d6-108">Beispiel 1: Aktivieren der Diagnose mithilfe eines in einer Diagnose Konfigurationsdatei angegebenen speicherkontos</span><span class="sxs-lookup"><span data-stu-id="e01d6-108">Example 1: Enable diagnostics using a storage account specified in a diagnostics configuration file</span></span>
```
PS C:\> Set-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup01" -VMName "VirtualMachine02" -DiagnosticsConfigurationPath "diagnostics_publicconfig.xml"
```

<span data-ttu-id="e01d6-109">Dieser Befehl verwendet eine Diagnose-Konfigurationsdatei, um die Diagnose zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="e01d6-109">This command uses a diagnostics configuration file to enable diagnostics.</span></span>
<span data-ttu-id="e01d6-110">Die Datei diagnostics_publicconfig.xml enthält die öffentliche XML-Konfiguration für die Diagnose Erweiterung, einschließlich des Namens des speicherkontos, an das Diagnosedaten gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="e01d6-110">The file diagnostics_publicconfig.xml contains the public XML configuration for the diagnostics extension including the name of the storage account to which diagnostics data will be sent.</span></span>
<span data-ttu-id="e01d6-111">Das Diagnosespeicher Konto muss sich im gleichen Abonnement wie der virtuelle Computer befinden.</span><span class="sxs-lookup"><span data-stu-id="e01d6-111">The diagnostics storage account must be in the same subscription as the virtual machine.</span></span>

### <span data-ttu-id="e01d6-112">Beispiel 2: Aktivieren der Diagnose mithilfe eines Speicherkonto namens</span><span class="sxs-lookup"><span data-stu-id="e01d6-112">Example 2: Enable diagnostics using a storage account name</span></span>
```
PS C:\> Set-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup1" -VMName "VirtualMachine2" -DiagnosticsConfigurationPath diagnostics_publicconfig.xml -StorageAccountName "MyStorageAccount"
```

<span data-ttu-id="e01d6-113">Dieser Befehl verwendet den Namen des speicherkontos, um die Diagnose zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="e01d6-113">This command uses the storage account name to enable diagnostics.</span></span>
<span data-ttu-id="e01d6-114">Wenn in der Diagnose Konfiguration kein Speicherkonto Name angegeben wird oder Sie den in der Konfigurationsdatei angegebenen Namen des Diagnosespeicher Kontos außer Kraft setzen möchten, verwenden Sie den Parameter *StorageAccountName* .</span><span class="sxs-lookup"><span data-stu-id="e01d6-114">If the diagnostics configuration does not specify a storage account name or if you want to override the diagnostics storage account name specified in the configuration file, use the *StorageAccountName* parameter.</span></span>
<span data-ttu-id="e01d6-115">Das Diagnosespeicher Konto muss sich im gleichen Abonnement wie der virtuelle Computer befinden.</span><span class="sxs-lookup"><span data-stu-id="e01d6-115">The diagnostics storage account must be in the same subscription as the virtual machine.</span></span>

### <span data-ttu-id="e01d6-116">Beispiel 3: Aktivieren der Diagnose mit dem Namen und Schlüssel des speicherkontos</span><span class="sxs-lookup"><span data-stu-id="e01d6-116">Example 3: Enable diagnostics using storage account name and key</span></span>
```
PS C:\> Set-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup01" -VMName "VirtualMachine02" -DiagnosticsConfigurationPath "diagnostics_publicconfig.xml" -StorageAccountName "MyStorageAccount" -StorageAccountKey $storage_key
```

<span data-ttu-id="e01d6-117">Dieser Befehl verwendet den Namen und den Schlüssel des speicherkontos, um die Diagnose zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="e01d6-117">This command uses the storage account name and key to enable diagnostics.</span></span>
<span data-ttu-id="e01d6-118">Wenn sich das Diagnosespeicher Konto in einem anderen Abonnement als der virtuelle Computer befindet, aktivieren Sie das Senden von Diagnosedaten an dieses Speicherkonto, indem Sie den Namen und den Schlüssel explizit angeben.</span><span class="sxs-lookup"><span data-stu-id="e01d6-118">If the diagnostics storage account is in a different subscription than the virtual machine then enable sending diagnostics data to that storage account by explicitly specifying its name and key.</span></span>

## <span data-ttu-id="e01d6-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="e01d6-119">PARAMETERS</span></span>

### <span data-ttu-id="e01d6-120">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="e01d6-120">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="e01d6-121">Gibt an, ob mit diesem Cmdlet der Azure Guest-Agent die Erweiterung automatisch auf eine neuere Nebenversion aktualisieren kann.</span><span class="sxs-lookup"><span data-stu-id="e01d6-121">Indicates whether this cmdlet allows the Azure guest agent to automatically update the extension to a newer minor version.</span></span>

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

### <span data-ttu-id="e01d6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e01d6-122">-DefaultProfile</span></span>
<span data-ttu-id="e01d6-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e01d6-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e01d6-124">-DiagnosticsConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="e01d6-124">-DiagnosticsConfigurationPath</span></span>
<span data-ttu-id="e01d6-125">Gibt den Pfad der Konfigurationsdatei an.</span><span class="sxs-lookup"><span data-stu-id="e01d6-125">Specifies the path of the configuration file.</span></span>

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

### <span data-ttu-id="e01d6-126">-Standort</span><span class="sxs-lookup"><span data-stu-id="e01d6-126">-Location</span></span>
<span data-ttu-id="e01d6-127">Gibt den Speicherort der virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="e01d6-127">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="e01d6-128">-Name</span><span class="sxs-lookup"><span data-stu-id="e01d6-128">-Name</span></span>
<span data-ttu-id="e01d6-129">Gibt den Namen einer Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="e01d6-129">Specifies the name of an extension.</span></span>

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

### <span data-ttu-id="e01d6-130">-Nowait</span><span class="sxs-lookup"><span data-stu-id="e01d6-130">-NoWait</span></span>
<span data-ttu-id="e01d6-131">Startet den Vorgang und gibt unmittelbar vor dem Abschluss des Vorgangs zurück.</span><span class="sxs-lookup"><span data-stu-id="e01d6-131">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="e01d6-132">Verwenden Sie einen anderen Mechanismus, um festzustellen, ob der Vorgang erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="e01d6-132">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="e01d6-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e01d6-133">-ResourceGroupName</span></span>
<span data-ttu-id="e01d6-134">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="e01d6-134">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="e01d6-135">-StorageAccountEndpoint</span><span class="sxs-lookup"><span data-stu-id="e01d6-135">-StorageAccountEndpoint</span></span>
<span data-ttu-id="e01d6-136">Gibt den Endpunkt des speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="e01d6-136">Specifies the storage account endpoint.</span></span>

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

### <span data-ttu-id="e01d6-137">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="e01d6-137">-StorageAccountKey</span></span>
<span data-ttu-id="e01d6-138">Gibt den speicherkontoschlüssel an.</span><span class="sxs-lookup"><span data-stu-id="e01d6-138">Specifies the storage account key.</span></span>

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

### <span data-ttu-id="e01d6-139">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="e01d6-139">-StorageAccountName</span></span>
<span data-ttu-id="e01d6-140">Gibt den Namen des speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="e01d6-140">Specifies the storage account name.</span></span>

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

### <span data-ttu-id="e01d6-141">-Storagecontext</span><span class="sxs-lookup"><span data-stu-id="e01d6-141">-StorageContext</span></span>
<span data-ttu-id="e01d6-142">Gibt den Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="e01d6-142">Specifies the Azure storage context.</span></span>

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

### <span data-ttu-id="e01d6-143">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="e01d6-143">-TypeHandlerVersion</span></span>
<span data-ttu-id="e01d6-144">Gibt die Version der Erweiterung an, die für diesen virtuellen Computer verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e01d6-144">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="e01d6-145">Führen Sie zum Abrufen der Version das Get-AzVMExtensionImage-Cmdlet mit dem Wert Microsoft. Compute für den *PublisherName* -Parameter und VMAccessAgent für den *Type* -Parameter aus.</span><span class="sxs-lookup"><span data-stu-id="e01d6-145">To obtain the version, run the Get-AzVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and VMAccessAgent for the *Type* parameter.</span></span>

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

### <span data-ttu-id="e01d6-146">-VMName</span><span class="sxs-lookup"><span data-stu-id="e01d6-146">-VMName</span></span>
<span data-ttu-id="e01d6-147">Gibt den Namen des virtuellen Computers an, auf dem dieses Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e01d6-147">Specifies the name of the virtual machine on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="e01d6-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e01d6-148">CommonParameters</span></span>
<span data-ttu-id="e01d6-149">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e01d6-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e01d6-150">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e01d6-150">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e01d6-151">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e01d6-151">INPUTS</span></span>

### <span data-ttu-id="e01d6-152">System. String</span><span class="sxs-lookup"><span data-stu-id="e01d6-152">System.String</span></span>

### <span data-ttu-id="e01d6-153">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="e01d6-153">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

### <span data-ttu-id="e01d6-154">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e01d6-154">System.Boolean</span></span>

## <span data-ttu-id="e01d6-155">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e01d6-155">OUTPUTS</span></span>

### <span data-ttu-id="e01d6-156">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="e01d6-156">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="e01d6-157">Notizen</span><span class="sxs-lookup"><span data-stu-id="e01d6-157">NOTES</span></span>

## <span data-ttu-id="e01d6-158">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e01d6-158">RELATED LINKS</span></span>

[<span data-ttu-id="e01d6-159">Get-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="e01d6-159">Get-AzVMDiagnosticsExtension</span></span>](./Get-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="e01d6-160">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="e01d6-160">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)

[<span data-ttu-id="e01d6-161">Remove-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="e01d6-161">Remove-AzVMDiagnosticsExtension</span></span>](./Remove-AzVMDiagnosticsExtension.md)



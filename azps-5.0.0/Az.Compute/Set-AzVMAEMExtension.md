---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3B15C734-DF57-433A-8854-ACE2B35FF6CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMAEMExtension.md
ms.openlocfilehash: b476254d5b9236aa95a30832499aca65a8a110c0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94296560"
---
# <span data-ttu-id="a7244-101">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="a7244-101">Set-AzVMAEMExtension</span></span>

## <span data-ttu-id="a7244-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a7244-102">SYNOPSIS</span></span>
<span data-ttu-id="a7244-103">Ermöglicht die Unterstützung für die Überwachung von SAP-Systemen.</span><span class="sxs-lookup"><span data-stu-id="a7244-103">Enables support for monitoring for SAP systems.</span></span>

## <span data-ttu-id="a7244-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a7244-104">SYNTAX</span></span>

```
Set-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [-EnableWAD]
 [[-WADStorageAccountName] <String>] [[-OSType] <String>] [-SkipStorage] [-NoWait]
 [-SetAccessToIndividualResources] [-InstallNewExtension] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a7244-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a7244-105">DESCRIPTION</span></span>
<span data-ttu-id="a7244-106">Das Cmdlet " **Satz-AzVMAEMExtension** " aktualisiert die Konfiguration einer virtuellen Maschine, um die Unterstützung für die Überwachung von SAP-Systemen zu aktivieren oder zu aktualisieren, die auf dem virtuellen Computer installiert sind.</span><span class="sxs-lookup"><span data-stu-id="a7244-106">The **Set-AzVMAEMExtension** cmdlet updates the configuration of a virtual machine to enable or update the support for monitoring for SAP systems that are installed on the virtual machine.</span></span>
<span data-ttu-id="a7244-107">Das Cmdlet installiert die Erweiterung Azure Enhanced Monitoring (AEM), die die Leistungsdaten erfasst und für das SAP-System auffindbar macht.</span><span class="sxs-lookup"><span data-stu-id="a7244-107">The cmdlet installs the Azure Enhanced Monitoring (AEM) extension that collects the performance data and makes it discoverable for the SAP system.</span></span>

## <span data-ttu-id="a7244-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a7244-108">EXAMPLES</span></span>

### <span data-ttu-id="a7244-109">Beispiel 1: Verwenden der AEM-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="a7244-109">Example 1: Use AEM extension</span></span>
```
PS C:\> Set-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server" -WADStorageAccountName "stdstorage"
```

<span data-ttu-id="a7244-110">Dieser Befehl konfiguriert den virtuellen Computer mit dem Namen "Contoso-Server", um die AEM-Erweiterung zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="a7244-110">This command configures the virtual machine named contoso-server to use the AEM extension.</span></span>
<span data-ttu-id="a7244-111">Der Befehl gibt das Speicherkonto mit dem Namen "stdstorage" an.</span><span class="sxs-lookup"><span data-stu-id="a7244-111">The command specifies the storage account named stdstorage.</span></span>

## <span data-ttu-id="a7244-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="a7244-112">PARAMETERS</span></span>

### <span data-ttu-id="a7244-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7244-113">-DefaultProfile</span></span>
<span data-ttu-id="a7244-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a7244-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a7244-115">-EnableWAD</span><span class="sxs-lookup"><span data-stu-id="a7244-115">-EnableWAD</span></span>
<span data-ttu-id="a7244-116">Wenn dieser Parameter bereitgestellt wird, aktiviert der Unifiedgroup Windows Azure-Diagnose für diesen virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="a7244-116">If this parameter is provided, the commandlet will enable Windows Azure Diagnostics for this virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7244-117">-InstallNewExtension</span><span class="sxs-lookup"><span data-stu-id="a7244-117">-InstallNewExtension</span></span>
<span data-ttu-id="a7244-118">Installieren Sie die neue VM-Erweiterung für SAP.</span><span class="sxs-lookup"><span data-stu-id="a7244-118">Install the new VM Extension for SAP.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7244-119">-Nowait</span><span class="sxs-lookup"><span data-stu-id="a7244-119">-NoWait</span></span>
<span data-ttu-id="a7244-120">Startet den Vorgang und gibt unmittelbar vor dem Abschluss des Vorgangs zurück.</span><span class="sxs-lookup"><span data-stu-id="a7244-120">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="a7244-121">Verwenden Sie einen anderen Mechanismus, um festzustellen, ob der Vorgang erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="a7244-121">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="a7244-122">-OSType</span><span class="sxs-lookup"><span data-stu-id="a7244-122">-OSType</span></span>
<span data-ttu-id="a7244-123">Gibt den Typ des Betriebssystems des Betriebssystemdatenträgers an.</span><span class="sxs-lookup"><span data-stu-id="a7244-123">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="a7244-124">Wenn auf dem Betriebssystemdatenträger kein Typ vorhanden ist, müssen Sie diesen Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="a7244-124">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="a7244-125">Die akzeptablen Werte für diesen Parameter sind: Windows und Linux.</span><span class="sxs-lookup"><span data-stu-id="a7244-125">The acceptable values for this parameter are: Windows and Linux.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7244-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7244-126">-ResourceGroupName</span></span>
<span data-ttu-id="a7244-127">Gibt den Namen der Ressourcengruppe des virtuellen Computers an, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="a7244-127">Specifies the name of the resource group of the virtual machine that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="a7244-128">-SetAccessToIndividualResources</span><span class="sxs-lookup"><span data-stu-id="a7244-128">-SetAccessToIndividualResources</span></span>
<span data-ttu-id="a7244-129">Legt den Zugriff auf die VM-Identität auf die einzelnen Ressourcen fest, beispielsweise auf Datenträger anstelle der vollständigen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a7244-129">Sets the access of the VM identity to the individual resources, e.g. data disks instead of the complete resource group.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7244-130">-SkipStorage</span><span class="sxs-lookup"><span data-stu-id="a7244-130">-SkipStorage</span></span>
<span data-ttu-id="a7244-131">Gibt an, dass dieses Cmdlet die Konfiguration des Speichers überspringt.</span><span class="sxs-lookup"><span data-stu-id="a7244-131">Indicates that this cmdlet skips configuration of storage.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7244-132">-VMName</span><span class="sxs-lookup"><span data-stu-id="a7244-132">-VMName</span></span>
<span data-ttu-id="a7244-133">Gibt den Namen einer virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="a7244-133">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="a7244-134">Mit diesem Cmdlet wird die AEM-Erweiterung für den virtuellen Computer, den dieser Parameter angibt, hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a7244-134">This cmdlet adds the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="a7244-135">-WADStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="a7244-135">-WADStorageAccountName</span></span>
<span data-ttu-id="a7244-136">Gibt den Namen des speicherkontos an, das dieses Cmdlet zum Konfigurieren der LinuxDiagnostics-oder IaaSDiagnostics-Erweiterung verwendet.</span><span class="sxs-lookup"><span data-stu-id="a7244-136">Specifies the name of the storage account that this cmdlet uses to configure the LinuxDiagnostics or IaaSDiagnostics extension.</span></span>
<span data-ttu-id="a7244-137">Wenn auf dem virtuellen Computer kein Standardspeicher Konto verwendet wird, müssen Sie einen Wert für diesen Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="a7244-137">If the virtual machine does not use a standard storage account, you must specify a value for this parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7244-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7244-138">CommonParameters</span></span>
<span data-ttu-id="a7244-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7244-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7244-140">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a7244-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7244-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a7244-141">INPUTS</span></span>

### <span data-ttu-id="a7244-142">System. String</span><span class="sxs-lookup"><span data-stu-id="a7244-142">System.String</span></span>

## <span data-ttu-id="a7244-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a7244-143">OUTPUTS</span></span>

### <span data-ttu-id="a7244-144">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="a7244-144">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="a7244-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="a7244-145">NOTES</span></span>

## <span data-ttu-id="a7244-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a7244-146">RELATED LINKS</span></span>

[<span data-ttu-id="a7244-147">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="a7244-147">Get-AzVMAEMExtension</span></span>](./Get-AzVMAEMExtension.md)

[<span data-ttu-id="a7244-148">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="a7244-148">Remove-AzVMAEMExtension</span></span>](./Remove-AzVMAEMExtension.md)

[<span data-ttu-id="a7244-149">Test-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="a7244-149">Test-AzVMAEMExtension</span></span>](./Test-AzVMAEMExtension.md)



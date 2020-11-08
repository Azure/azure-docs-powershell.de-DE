---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3B15C734-DF57-433A-8854-ACE2B35FF6CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMAEMExtension.md
ms.openlocfilehash: b476254d5b9236aa95a30832499aca65a8a110c0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173292"
---
# <span data-ttu-id="c2475-101">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="c2475-101">Set-AzVMAEMExtension</span></span>

## <span data-ttu-id="c2475-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c2475-102">SYNOPSIS</span></span>
<span data-ttu-id="c2475-103">Ermöglicht die Unterstützung für die Überwachung von SAP-Systemen.</span><span class="sxs-lookup"><span data-stu-id="c2475-103">Enables support for monitoring for SAP systems.</span></span>

## <span data-ttu-id="c2475-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c2475-104">SYNTAX</span></span>

```
Set-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [-EnableWAD]
 [[-WADStorageAccountName] <String>] [[-OSType] <String>] [-SkipStorage] [-NoWait]
 [-SetAccessToIndividualResources] [-InstallNewExtension] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c2475-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c2475-105">DESCRIPTION</span></span>
<span data-ttu-id="c2475-106">Das Cmdlet " **Satz-AzVMAEMExtension** " aktualisiert die Konfiguration einer virtuellen Maschine, um die Unterstützung für die Überwachung von SAP-Systemen zu aktivieren oder zu aktualisieren, die auf dem virtuellen Computer installiert sind.</span><span class="sxs-lookup"><span data-stu-id="c2475-106">The **Set-AzVMAEMExtension** cmdlet updates the configuration of a virtual machine to enable or update the support for monitoring for SAP systems that are installed on the virtual machine.</span></span>
<span data-ttu-id="c2475-107">Das Cmdlet installiert die Erweiterung Azure Enhanced Monitoring (AEM), die die Leistungsdaten erfasst und für das SAP-System auffindbar macht.</span><span class="sxs-lookup"><span data-stu-id="c2475-107">The cmdlet installs the Azure Enhanced Monitoring (AEM) extension that collects the performance data and makes it discoverable for the SAP system.</span></span>

## <span data-ttu-id="c2475-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c2475-108">EXAMPLES</span></span>

### <span data-ttu-id="c2475-109">Beispiel 1: Verwenden der AEM-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="c2475-109">Example 1: Use AEM extension</span></span>
```
PS C:\> Set-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server" -WADStorageAccountName "stdstorage"
```

<span data-ttu-id="c2475-110">Dieser Befehl konfiguriert den virtuellen Computer mit dem Namen "Contoso-Server", um die AEM-Erweiterung zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="c2475-110">This command configures the virtual machine named contoso-server to use the AEM extension.</span></span>
<span data-ttu-id="c2475-111">Der Befehl gibt das Speicherkonto mit dem Namen "stdstorage" an.</span><span class="sxs-lookup"><span data-stu-id="c2475-111">The command specifies the storage account named stdstorage.</span></span>

## <span data-ttu-id="c2475-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="c2475-112">PARAMETERS</span></span>

### <span data-ttu-id="c2475-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2475-113">-DefaultProfile</span></span>
<span data-ttu-id="c2475-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c2475-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c2475-115">-EnableWAD</span><span class="sxs-lookup"><span data-stu-id="c2475-115">-EnableWAD</span></span>
<span data-ttu-id="c2475-116">Wenn dieser Parameter bereitgestellt wird, aktiviert der Unifiedgroup Windows Azure-Diagnose für diesen virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="c2475-116">If this parameter is provided, the commandlet will enable Windows Azure Diagnostics for this virtual machine.</span></span>

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

### <span data-ttu-id="c2475-117">-InstallNewExtension</span><span class="sxs-lookup"><span data-stu-id="c2475-117">-InstallNewExtension</span></span>
<span data-ttu-id="c2475-118">Installieren Sie die neue VM-Erweiterung für SAP.</span><span class="sxs-lookup"><span data-stu-id="c2475-118">Install the new VM Extension for SAP.</span></span>

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

### <span data-ttu-id="c2475-119">-Nowait</span><span class="sxs-lookup"><span data-stu-id="c2475-119">-NoWait</span></span>
<span data-ttu-id="c2475-120">Startet den Vorgang und gibt unmittelbar vor dem Abschluss des Vorgangs zurück.</span><span class="sxs-lookup"><span data-stu-id="c2475-120">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="c2475-121">Verwenden Sie einen anderen Mechanismus, um festzustellen, ob der Vorgang erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="c2475-121">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="c2475-122">-OSType</span><span class="sxs-lookup"><span data-stu-id="c2475-122">-OSType</span></span>
<span data-ttu-id="c2475-123">Gibt den Typ des Betriebssystems des Betriebssystemdatenträgers an.</span><span class="sxs-lookup"><span data-stu-id="c2475-123">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="c2475-124">Wenn auf dem Betriebssystemdatenträger kein Typ vorhanden ist, müssen Sie diesen Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="c2475-124">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="c2475-125">Die akzeptablen Werte für diesen Parameter sind: Windows und Linux.</span><span class="sxs-lookup"><span data-stu-id="c2475-125">The acceptable values for this parameter are: Windows and Linux.</span></span>

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

### <span data-ttu-id="c2475-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2475-126">-ResourceGroupName</span></span>
<span data-ttu-id="c2475-127">Gibt den Namen der Ressourcengruppe des virtuellen Computers an, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="c2475-127">Specifies the name of the resource group of the virtual machine that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="c2475-128">-SetAccessToIndividualResources</span><span class="sxs-lookup"><span data-stu-id="c2475-128">-SetAccessToIndividualResources</span></span>
<span data-ttu-id="c2475-129">Legt den Zugriff auf die VM-Identität auf die einzelnen Ressourcen fest, beispielsweise auf Datenträger anstelle der vollständigen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c2475-129">Sets the access of the VM identity to the individual resources, e.g. data disks instead of the complete resource group.</span></span>

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

### <span data-ttu-id="c2475-130">-SkipStorage</span><span class="sxs-lookup"><span data-stu-id="c2475-130">-SkipStorage</span></span>
<span data-ttu-id="c2475-131">Gibt an, dass dieses Cmdlet die Konfiguration des Speichers überspringt.</span><span class="sxs-lookup"><span data-stu-id="c2475-131">Indicates that this cmdlet skips configuration of storage.</span></span>

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

### <span data-ttu-id="c2475-132">-VMName</span><span class="sxs-lookup"><span data-stu-id="c2475-132">-VMName</span></span>
<span data-ttu-id="c2475-133">Gibt den Namen einer virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="c2475-133">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="c2475-134">Mit diesem Cmdlet wird die AEM-Erweiterung für den virtuellen Computer, den dieser Parameter angibt, hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="c2475-134">This cmdlet adds the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="c2475-135">-WADStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="c2475-135">-WADStorageAccountName</span></span>
<span data-ttu-id="c2475-136">Gibt den Namen des speicherkontos an, das dieses Cmdlet zum Konfigurieren der LinuxDiagnostics-oder IaaSDiagnostics-Erweiterung verwendet.</span><span class="sxs-lookup"><span data-stu-id="c2475-136">Specifies the name of the storage account that this cmdlet uses to configure the LinuxDiagnostics or IaaSDiagnostics extension.</span></span>
<span data-ttu-id="c2475-137">Wenn auf dem virtuellen Computer kein Standardspeicher Konto verwendet wird, müssen Sie einen Wert für diesen Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="c2475-137">If the virtual machine does not use a standard storage account, you must specify a value for this parameter.</span></span>

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

### <span data-ttu-id="c2475-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2475-138">CommonParameters</span></span>
<span data-ttu-id="c2475-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2475-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2475-140">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c2475-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2475-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c2475-141">INPUTS</span></span>

### <span data-ttu-id="c2475-142">System. String</span><span class="sxs-lookup"><span data-stu-id="c2475-142">System.String</span></span>

## <span data-ttu-id="c2475-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c2475-143">OUTPUTS</span></span>

### <span data-ttu-id="c2475-144">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="c2475-144">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="c2475-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="c2475-145">NOTES</span></span>

## <span data-ttu-id="c2475-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c2475-146">RELATED LINKS</span></span>

[<span data-ttu-id="c2475-147">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="c2475-147">Get-AzVMAEMExtension</span></span>](./Get-AzVMAEMExtension.md)

[<span data-ttu-id="c2475-148">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="c2475-148">Remove-AzVMAEMExtension</span></span>](./Remove-AzVMAEMExtension.md)

[<span data-ttu-id="c2475-149">Test-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="c2475-149">Test-AzVMAEMExtension</span></span>](./Test-AzVMAEMExtension.md)



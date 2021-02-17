---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3B15C734-DF57-433A-8854-ACE2B35FF6CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMAEMExtension.md
ms.openlocfilehash: b476254d5b9236aa95a30832499aca65a8a110c0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100175905"
---
# <span data-ttu-id="f60fb-101">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="f60fb-101">Set-AzVMAEMExtension</span></span>

## <span data-ttu-id="f60fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f60fb-102">SYNOPSIS</span></span>
<span data-ttu-id="f60fb-103">Ermöglicht die Unterstützung der Überwachung für SAP-Systeme.</span><span class="sxs-lookup"><span data-stu-id="f60fb-103">Enables support for monitoring for SAP systems.</span></span>

## <span data-ttu-id="f60fb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f60fb-104">SYNTAX</span></span>

```
Set-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [-EnableWAD]
 [[-WADStorageAccountName] <String>] [[-OSType] <String>] [-SkipStorage] [-NoWait]
 [-SetAccessToIndividualResources] [-InstallNewExtension] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f60fb-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f60fb-105">DESCRIPTION</span></span>
<span data-ttu-id="f60fb-106">Das **Cmdlet "Set-AzVMAEMExtension"** aktualisiert die Konfiguration eines virtuellen Computers, um die Unterstützung für die Überwachung von SAP-Systemen zu aktivieren oder zu aktualisieren, die auf dem virtuellen Computer installiert sind.</span><span class="sxs-lookup"><span data-stu-id="f60fb-106">The **Set-AzVMAEMExtension** cmdlet updates the configuration of a virtual machine to enable or update the support for monitoring for SAP systems that are installed on the virtual machine.</span></span>
<span data-ttu-id="f60fb-107">Das Cmdlet installiert die Azure Enhanced Monitoring (AEM)-Erweiterung, mit der die Leistungsdaten gesammelt und für das SAP-System aufs neue System zu finden sind.</span><span class="sxs-lookup"><span data-stu-id="f60fb-107">The cmdlet installs the Azure Enhanced Monitoring (AEM) extension that collects the performance data and makes it discoverable for the SAP system.</span></span>

## <span data-ttu-id="f60fb-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f60fb-108">EXAMPLES</span></span>

### <span data-ttu-id="f60fb-109">Beispiel 1: Verwenden der Erweiterung AEM</span><span class="sxs-lookup"><span data-stu-id="f60fb-109">Example 1: Use AEM extension</span></span>
```
PS C:\> Set-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server" -WADStorageAccountName "stdstorage"
```

<span data-ttu-id="f60fb-110">Mit diesem Befehl wird der virtuelle Computer "contoso-server" so konfiguriert, dass die Erweiterung AEM verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f60fb-110">This command configures the virtual machine named contoso-server to use the AEM extension.</span></span>
<span data-ttu-id="f60fb-111">Der Befehl gibt das Speicherkonto "stdstorage" an.</span><span class="sxs-lookup"><span data-stu-id="f60fb-111">The command specifies the storage account named stdstorage.</span></span>

## <span data-ttu-id="f60fb-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f60fb-112">PARAMETERS</span></span>

### <span data-ttu-id="f60fb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f60fb-113">-DefaultProfile</span></span>
<span data-ttu-id="f60fb-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f60fb-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f60fb-115">-EnableWAD</span><span class="sxs-lookup"><span data-stu-id="f60fb-115">-EnableWAD</span></span>
<span data-ttu-id="f60fb-116">Wenn dieser Parameter bereitgestellt wird, aktiviert das Commandlet Windows Azure Diagnose für diesen virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="f60fb-116">If this parameter is provided, the commandlet will enable Windows Azure Diagnostics for this virtual machine.</span></span>

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

### <span data-ttu-id="f60fb-117">-InstallNewExtension</span><span class="sxs-lookup"><span data-stu-id="f60fb-117">-InstallNewExtension</span></span>
<span data-ttu-id="f60fb-118">Installieren Sie die neue VM Extension für SAP.</span><span class="sxs-lookup"><span data-stu-id="f60fb-118">Install the new VM Extension for SAP.</span></span>

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

### <span data-ttu-id="f60fb-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="f60fb-119">-NoWait</span></span>
<span data-ttu-id="f60fb-120">Der Vorgang wird gestartet und unmittelbar vor Abschluss des Vorgangs beendet.</span><span class="sxs-lookup"><span data-stu-id="f60fb-120">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="f60fb-121">Verwenden Sie einen anderen Mechanismus, um festzustellen, ob der Vorgang erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="f60fb-121">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="f60fb-122">-OSType</span><span class="sxs-lookup"><span data-stu-id="f60fb-122">-OSType</span></span>
<span data-ttu-id="f60fb-123">Gibt den Typ des Betriebssystems des Betriebssystemdatenträgers an.</span><span class="sxs-lookup"><span data-stu-id="f60fb-123">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="f60fb-124">Wenn der Betriebssystemdatenträger keinen Typ hat, müssen Sie diesen Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="f60fb-124">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="f60fb-125">Die zulässigen Werte für diesen Parameter sind: Windows und Linux.</span><span class="sxs-lookup"><span data-stu-id="f60fb-125">The acceptable values for this parameter are: Windows and Linux.</span></span>

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

### <span data-ttu-id="f60fb-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f60fb-126">-ResourceGroupName</span></span>
<span data-ttu-id="f60fb-127">Gibt den Namen der Ressourcengruppe des virtuellen Computers an, den dieses Cmdlet ändert.</span><span class="sxs-lookup"><span data-stu-id="f60fb-127">Specifies the name of the resource group of the virtual machine that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="f60fb-128">-SetAccessToIndividualResources</span><span class="sxs-lookup"><span data-stu-id="f60fb-128">-SetAccessToIndividualResources</span></span>
<span data-ttu-id="f60fb-129">Legt den Zugriff der Identität der VM auf die einzelnen Ressourcen fest, z. B. Datenträger anstelle der vollständigen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f60fb-129">Sets the access of the VM identity to the individual resources, e.g. data disks instead of the complete resource group.</span></span>

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

### <span data-ttu-id="f60fb-130">-SkipStorage</span><span class="sxs-lookup"><span data-stu-id="f60fb-130">-SkipStorage</span></span>
<span data-ttu-id="f60fb-131">Gibt an, dass dieses Cmdlet die Speicherkonfiguration überspringt.</span><span class="sxs-lookup"><span data-stu-id="f60fb-131">Indicates that this cmdlet skips configuration of storage.</span></span>

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

### <span data-ttu-id="f60fb-132">-VMName</span><span class="sxs-lookup"><span data-stu-id="f60fb-132">-VMName</span></span>
<span data-ttu-id="f60fb-133">Gibt den Namen eines virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="f60fb-133">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="f60fb-134">Dieses Cmdlet fügt die AEM-Erweiterung für den virtuellen Computer hinzu, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="f60fb-134">This cmdlet adds the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="f60fb-135">-WADStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="f60fb-135">-WADStorageAccountName</span></span>
<span data-ttu-id="f60fb-136">Gibt den Namen des Speicherkontos an, das von diesem Cmdlet zum Konfigurieren der Erweiterung LinuxDiagnostics oder IaaSDiagnostics verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f60fb-136">Specifies the name of the storage account that this cmdlet uses to configure the LinuxDiagnostics or IaaSDiagnostics extension.</span></span>
<span data-ttu-id="f60fb-137">Wenn der virtuelle Computer kein Standardspeicherkonto verwendet, müssen Sie einen Wert für diesen Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="f60fb-137">If the virtual machine does not use a standard storage account, you must specify a value for this parameter.</span></span>

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

### <span data-ttu-id="f60fb-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f60fb-138">CommonParameters</span></span>
<span data-ttu-id="f60fb-139">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f60fb-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f60fb-140">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f60fb-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f60fb-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f60fb-141">INPUTS</span></span>

### <span data-ttu-id="f60fb-142">System.String</span><span class="sxs-lookup"><span data-stu-id="f60fb-142">System.String</span></span>

## <span data-ttu-id="f60fb-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f60fb-143">OUTPUTS</span></span>

### <span data-ttu-id="f60fb-144">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="f60fb-144">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="f60fb-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f60fb-145">NOTES</span></span>

## <span data-ttu-id="f60fb-146">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f60fb-146">RELATED LINKS</span></span>

[<span data-ttu-id="f60fb-147">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="f60fb-147">Get-AzVMAEMExtension</span></span>](./Get-AzVMAEMExtension.md)

[<span data-ttu-id="f60fb-148">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="f60fb-148">Remove-AzVMAEMExtension</span></span>](./Remove-AzVMAEMExtension.md)

[<span data-ttu-id="f60fb-149">Test-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="f60fb-149">Test-AzVMAEMExtension</span></span>](./Test-AzVMAEMExtension.md)



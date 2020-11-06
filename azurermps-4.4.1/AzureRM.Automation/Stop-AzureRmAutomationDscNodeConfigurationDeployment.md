---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Stop-AzureRmAutomationDscNodeConfigurationDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Stop-AzureRmAutomationDscNodeConfigurationDeployment.md
ms.openlocfilehash: 3ddaf0d4ae609305bf9740fbbe38a5fddd414e18
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503273"
---
# <span data-ttu-id="ee176-101">Stop-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="ee176-101">Stop-AzureRmAutomationDscNodeConfigurationDeployment</span></span>

## <span data-ttu-id="ee176-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ee176-102">SYNOPSIS</span></span>
<span data-ttu-id="ee176-103">Beendet die Bereitstellung einer DSC-Knoten Konfiguration in der Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="ee176-103">Stops a DSC Node configuration deployment in Automation.</span></span> <span data-ttu-id="ee176-104">Der aktuelle Bereitstellungsauftrag wird nur beendet, aber die Zuweisung bereits zugewiesener Knoten Konfigurationen wird nicht aufheben.</span><span class="sxs-lookup"><span data-stu-id="ee176-104">It only stops the current deployment job but does not unassign already assigned node configurations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ee176-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ee176-105">SYNTAX</span></span>

### <span data-ttu-id="ee176-106">ByJobId (Standard)</span><span class="sxs-lookup"><span data-stu-id="ee176-106">ByJobId (Default)</span></span>
```
Stop-AzureRmAutomationDscNodeConfigurationDeployment -JobId <Guid> [-Force] [-PassThru]
 [-ResourceGroupName] <String> -AutomationAccountName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee176-107">ByByInputObject</span><span class="sxs-lookup"><span data-stu-id="ee176-107">ByByInputObject</span></span>
```
Stop-AzureRmAutomationDscNodeConfigurationDeployment [-PassThru] -InputObject <NodeConfigurationDeployment>
 [-ResourceGroupName] <String> -AutomationAccountName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee176-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ee176-108">DESCRIPTION</span></span>
<span data-ttu-id="ee176-109">Das Cmdlet " **Stop-AzureRmAutomationDscNodeConfigurationDeployment** " beendet die Bereitstellung einer Statuskonfiguration (DSC)-Knoten Konfiguration in Azure-Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="ee176-109">The **Stop-AzureRmAutomationDscNodeConfigurationDeployment** cmdlet stops a deployment of a Desired State Configuration (DSC) node configuration in Azure Automation.</span></span> <span data-ttu-id="ee176-110">Die Zuweisung der Knoten Konfiguration an Knotengruppen wird beendet, wenn eine solche zugewiesen werden soll, aber nicht die Zuweisung bereits zugewiesener Knoten aufheben.</span><span class="sxs-lookup"><span data-stu-id="ee176-110">It stops assignment of node configuration to groups of nodes, if any are remaining to be assigned, but does not unassign already assigned nodes.</span></span> <span data-ttu-id="ee176-111">Wenn Sie die Registrierung eines geplanten Auftrags aufheben möchten, verwenden Sie die [Unregister-AzureRmAutomationScheduledRunbook](./Unregister-AzureRmAutomationScheduledRunbook.md) mit dem JobScheduleId, um die Zuweisung eines vorhandenen geplanten Auftrags aufzuheben.</span><span class="sxs-lookup"><span data-stu-id="ee176-111">To unregister a scheduled job, please use the [Unregister-AzureRmAutomationScheduledRunbook](./Unregister-AzureRmAutomationScheduledRunbook.md) with the JobScheduleId to unassign an existing scheduled job.</span></span>

## <span data-ttu-id="ee176-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ee176-112">EXAMPLES</span></span>

### <span data-ttu-id="ee176-113">Beispiel 1: Bereitstelleneiner Azure DSC-Knoten Konfiguration in der Automatisierung</span><span class="sxs-lookup"><span data-stu-id="ee176-113">Example 1: Deploy an Azure DSC node configuration in Automation</span></span>
```
PS C:\> Stop-AzureRmAutomationDscNodeConfigurationDeployment -AutomationAccountName "Contoso01" -ResourceGroupName "ResourceGroup01" -JobId 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="ee176-114">Der obige Befehl beendet den Bereitstellungsauftrag für die DSC-Knoten Konfiguration mit dem übergebenen JobID.</span><span class="sxs-lookup"><span data-stu-id="ee176-114">The above command stops the DSC node configuration deployment job with the jobId passed in.</span></span>

## <span data-ttu-id="ee176-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="ee176-115">PARAMETERS</span></span>

### <span data-ttu-id="ee176-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ee176-116">-AutomationAccountName</span></span>
<span data-ttu-id="ee176-117">Gibt den Namen des Automatisierungs Kontos an, das die DSC-Konfiguration enthält, die von diesem Cmdlet kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="ee176-117">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee176-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee176-118">-ResourceGroupName</span></span>
<span data-ttu-id="ee176-119">Gibt den Namen einer Ressourcengruppe an, in der dieses Cmdlet eine Konfiguration kompiliert.</span><span class="sxs-lookup"><span data-stu-id="ee176-119">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="ee176-120">-JobId</span><span class="sxs-lookup"><span data-stu-id="ee176-120">-JobId</span></span>
<span data-ttu-id="ee176-121">Gibt die Auftrags-ID eines vorhandenen Bereitstellungsauftrags an.</span><span class="sxs-lookup"><span data-stu-id="ee176-121">Specifies the Job id of an existing deployment job.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ByJobId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee176-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ee176-122">-PassThru</span></span>
<span data-ttu-id="ee176-123">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="ee176-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ee176-124">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="ee176-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ee176-125">-Force</span><span class="sxs-lookup"><span data-stu-id="ee176-125">-Force</span></span>
<span data-ttu-id="ee176-126">ps_force</span><span class="sxs-lookup"><span data-stu-id="ee176-126">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByJobId
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee176-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ee176-127">-Confirm</span></span>
<span data-ttu-id="ee176-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ee176-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee176-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee176-129">-WhatIf</span></span>
<span data-ttu-id="ee176-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ee176-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee176-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ee176-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee176-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee176-132">-DefaultProfile</span></span>
<span data-ttu-id="ee176-133">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ee176-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee176-134">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ee176-134">-InputObject</span></span>
<span data-ttu-id="ee176-135">Eingabeobjekt für die Rohrverlegung</span><span class="sxs-lookup"><span data-stu-id="ee176-135">Input object for Piping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment
Parameter Sets: ByByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ee176-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee176-136">CommonParameters</span></span>
<span data-ttu-id="ee176-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee176-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee176-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee176-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee176-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ee176-139">INPUTS</span></span>

## <span data-ttu-id="ee176-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ee176-140">OUTPUTS</span></span>

## <span data-ttu-id="ee176-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="ee176-141">NOTES</span></span>

## <span data-ttu-id="ee176-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ee176-142">RELATED LINKS</span></span>

[<span data-ttu-id="ee176-143">Anfang-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="ee176-143">Start-AzureRmAutomationDscCompilationJob</span></span>](./Start-AzureRmAutomationDscCompilationJob.md)

[<span data-ttu-id="ee176-144">Importieren-AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="ee176-144">Import-AzureRmAutomationDscNodeConfiguration</span></span>](./Import-AzureRmAutomationDscNodeConfiguration.md)

[<span data-ttu-id="ee176-145">Anfang-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="ee176-145">Start-AzureRmAutomationDscNodeConfigurationDeployment</span></span>](./Start-AzureRmAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="ee176-146">Get-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="ee176-146">Get-AzureRmAutomationDscNodeConfigurationDeployment</span></span>](./Get-AzureRmAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="ee176-147">Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="ee176-147">Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule</span></span>](./Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule.md)

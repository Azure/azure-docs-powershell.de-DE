---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapselinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseLinkedService.md
ms.openlocfilehash: ca493914cc91d16566fddcebed5367fa81be1d2d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178119"
---
# <span data-ttu-id="897d5-101">Remove-AzSynapseLinkedService</span><span class="sxs-lookup"><span data-stu-id="897d5-101">Remove-AzSynapseLinkedService</span></span>

## <span data-ttu-id="897d5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="897d5-102">SYNOPSIS</span></span>
<span data-ttu-id="897d5-103">Entfernt einen verknüpften Dienst aus dem Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="897d5-103">Removes a linked service from workspace.</span></span>

## <span data-ttu-id="897d5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="897d5-104">SYNTAX</span></span>

### <span data-ttu-id="897d5-105">RemoveByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="897d5-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseLinkedService -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="897d5-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="897d5-106">RemoveByObject</span></span>
```
Remove-AzSynapseLinkedService -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="897d5-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="897d5-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseLinkedService -InputObject <PSLinkedServiceResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="897d5-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="897d5-108">DESCRIPTION</span></span>
<span data-ttu-id="897d5-109">Mit dem Cmdlet **Remove-AzSynapseLinkedService** wird ein verknüpfter Dienst aus dem Arbeitsbereich entfernt.</span><span class="sxs-lookup"><span data-stu-id="897d5-109">The **Remove-AzSynapseLinkedService** cmdlet removes a linked service from workspace.</span></span>

## <span data-ttu-id="897d5-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="897d5-110">EXAMPLES</span></span>

### <span data-ttu-id="897d5-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="897d5-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseLinkedService -WorkspaceName ContosoWorkspace -Name ContosoLinkedService
```

<span data-ttu-id="897d5-112">Mit diesem Befehl wird der verknüpfte Dienst mit dem Namen ContosoLinkedService aus dem Arbeitsbereich mit dem Namen ContosoWorkspace entfernt.</span><span class="sxs-lookup"><span data-stu-id="897d5-112">This command removes the linked service named ContosoLinkedService from the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="897d5-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="897d5-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseLinkedService -Name ContosoLinkedService
```

<span data-ttu-id="897d5-114">Mit diesem Befehl wird der verknüpfte Dienst mit dem Namen ContosoLinkedService aus dem Arbeitsbereich mit dem Namen ContosoWorkspace through Pipeline entfernt.</span><span class="sxs-lookup"><span data-stu-id="897d5-114">This command removes the linked service named ContosoLinkedService from the workspace named ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="897d5-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="897d5-115">Example 3</span></span>
```powershell
PS C:\> $linkedService = Get-AzSynapseLinkedService -WorkspaceName ContosoWorkspace -Name ContosoLinkedService
PS C:\> $linkedService | Remove-AzSynapseLinkedService
```

<span data-ttu-id="897d5-116">Mit diesem Befehl wird der verknüpfte Dienst mit dem Namen ContosoLinkedService aus dem Arbeitsbereich mit dem Namen ContosoWorkspace through Pipeline entfernt.</span><span class="sxs-lookup"><span data-stu-id="897d5-116">This command removes the linked service named ContosoLinkedService from the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="897d5-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="897d5-117">PARAMETERS</span></span>

### <span data-ttu-id="897d5-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="897d5-118">-AsJob</span></span>
<span data-ttu-id="897d5-119">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="897d5-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="897d5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="897d5-120">-DefaultProfile</span></span>
<span data-ttu-id="897d5-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="897d5-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="897d5-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="897d5-122">-InputObject</span></span>
<span data-ttu-id="897d5-123">Das verknüpfte Dienstobjekt.</span><span class="sxs-lookup"><span data-stu-id="897d5-123">The linked service object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="897d5-124">-Name</span><span class="sxs-lookup"><span data-stu-id="897d5-124">-Name</span></span>
<span data-ttu-id="897d5-125">Der Name des verknüpften Diensts.</span><span class="sxs-lookup"><span data-stu-id="897d5-125">The linked service name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName, RemoveByObject
Aliases: LinkedServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="897d5-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="897d5-126">-PassThru</span></span>
<span data-ttu-id="897d5-127">Dieses Cmdlet gibt standardmäßig kein Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="897d5-127">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="897d5-128">Wenn dieser Schalter angegeben wird, wird true zurückgegeben, wenn er erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="897d5-128">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="897d5-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="897d5-129">-WorkspaceName</span></span>
<span data-ttu-id="897d5-130">Name des Synapse-Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="897d5-130">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="897d5-131">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="897d5-131">-WorkspaceObject</span></span>
<span data-ttu-id="897d5-132">Arbeitsbereichs Eingabeobjekt, in der Regel durch die Pipeline übergeben.</span><span class="sxs-lookup"><span data-stu-id="897d5-132">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RemoveByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="897d5-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="897d5-133">-Confirm</span></span>
<span data-ttu-id="897d5-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="897d5-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="897d5-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="897d5-135">-WhatIf</span></span>
<span data-ttu-id="897d5-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="897d5-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="897d5-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="897d5-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="897d5-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="897d5-138">CommonParameters</span></span>
<span data-ttu-id="897d5-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="897d5-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="897d5-140">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="897d5-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="897d5-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="897d5-141">INPUTS</span></span>

### <span data-ttu-id="897d5-142">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="897d5-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="897d5-143">Microsoft. Azure. Commands. Synapse. Models. PSLinkedServiceResource</span><span class="sxs-lookup"><span data-stu-id="897d5-143">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span></span>

## <span data-ttu-id="897d5-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="897d5-144">OUTPUTS</span></span>

### <span data-ttu-id="897d5-145">Microsoft. Azure. Commands. Synapse. Models. PSLinkedServiceResource</span><span class="sxs-lookup"><span data-stu-id="897d5-145">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span></span>

## <span data-ttu-id="897d5-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="897d5-146">NOTES</span></span>

## <span data-ttu-id="897d5-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="897d5-147">RELATED LINKS</span></span>

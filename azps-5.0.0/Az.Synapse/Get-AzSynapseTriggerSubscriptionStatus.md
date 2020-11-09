---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsetriggersubscriptionstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTriggerSubscriptionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTriggerSubscriptionStatus.md
ms.openlocfilehash: b18a308b94bdb486945186c67c3a905bcb0408d3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301708"
---
# <span data-ttu-id="34aca-101">Get-AzSynapseTriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="34aca-101">Get-AzSynapseTriggerSubscriptionStatus</span></span>

## <span data-ttu-id="34aca-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="34aca-102">SYNOPSIS</span></span>
<span data-ttu-id="34aca-103">Abrufen des Status des Abonnements für den Ereignisauslöser für die angegebenen externen Dienstereignisse.</span><span class="sxs-lookup"><span data-stu-id="34aca-103">Get the status of the subscription for the event trigger to the specified external service events.</span></span>

## <span data-ttu-id="34aca-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="34aca-104">SYNTAX</span></span>

### <span data-ttu-id="34aca-105">GetByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="34aca-105">GetByName (Default)</span></span>
```
Get-AzSynapseTriggerSubscriptionStatus -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="34aca-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="34aca-106">GetByObject</span></span>
```
Get-AzSynapseTriggerSubscriptionStatus -WorkspaceObject <PSSynapseWorkspace> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="34aca-107">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="34aca-107">GetByInputObject</span></span>
```
Get-AzSynapseTriggerSubscriptionStatus -InputObject <PSTriggerResource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="34aca-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="34aca-108">DESCRIPTION</span></span>
<span data-ttu-id="34aca-109">Das Cmdlet " **Get-AzSynapseTriggerSubscriptionStatus** " Ruft den Status des Abonnements für den Ereignisauslöser für die angegebenen externen Dienstereignisse ab.</span><span class="sxs-lookup"><span data-stu-id="34aca-109">The **Get-AzSynapseTriggerSubscriptionStatus** cmdlet gets the status of the subscription for the event trigger to the specified external service events.</span></span> <span data-ttu-id="34aca-110">Der Trigger kann erst gestartet werden, wenn der zurückgegebene Status "aktiviert" ist.</span><span class="sxs-lookup"><span data-stu-id="34aca-110">The trigger can't be started until the returned status is "Enabled".</span></span>

## <span data-ttu-id="34aca-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="34aca-111">EXAMPLES</span></span>

### <span data-ttu-id="34aca-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="34aca-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseTriggerSubscriptionStatus -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="34aca-113">Dieser Befehl ruft den Status des Kontroll für Trigger ab, der als ContosoTrigger für externe Dienstereignisse bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="34aca-113">This command will get the status of the subscribtion for trigger called ContosoTrigger to the external service events.</span></span>

### <span data-ttu-id="34aca-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="34aca-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseTriggerSubscriptionStatus -Name ContosoTrigger
```

<span data-ttu-id="34aca-115">Dieser Befehl ruft den Status des Kontroll for Triggers ab, der als ContosoTrigger für externe Dienstereignisse durch Pipeline bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="34aca-115">This command will get the status of the subscribtion for trigger called ContosoTrigger to the external service events through pipeline.</span></span>

### <span data-ttu-id="34aca-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="34aca-116">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Get-AzSynapseTriggerSubscriptionStatus
```

<span data-ttu-id="34aca-117">Dieser Befehl ruft den Status des Kontroll for Triggers ab, der als ContosoTrigger für externe Dienstereignisse durch Pipeline bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="34aca-117">This command will get the status of the subscribtion for trigger called ContosoTrigger to the external service events through pipeline.</span></span>

## <span data-ttu-id="34aca-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="34aca-118">PARAMETERS</span></span>

### <span data-ttu-id="34aca-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34aca-119">-DefaultProfile</span></span>
<span data-ttu-id="34aca-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="34aca-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34aca-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="34aca-121">-InputObject</span></span>
<span data-ttu-id="34aca-122">Das Trigger-Objekt.</span><span class="sxs-lookup"><span data-stu-id="34aca-122">The trigger object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource
Parameter Sets: GetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="34aca-123">-Name</span><span class="sxs-lookup"><span data-stu-id="34aca-123">-Name</span></span>
<span data-ttu-id="34aca-124">Der Name des Triggers.</span><span class="sxs-lookup"><span data-stu-id="34aca-124">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName, GetByObject
Aliases: TriggerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34aca-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="34aca-125">-WorkspaceName</span></span>
<span data-ttu-id="34aca-126">Name des Synapse-Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="34aca-126">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34aca-127">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="34aca-127">-WorkspaceObject</span></span>
<span data-ttu-id="34aca-128">Arbeitsbereichs Eingabeobjekt, in der Regel durch die Pipeline übergeben.</span><span class="sxs-lookup"><span data-stu-id="34aca-128">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="34aca-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34aca-129">CommonParameters</span></span>
<span data-ttu-id="34aca-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34aca-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34aca-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="34aca-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34aca-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="34aca-132">INPUTS</span></span>

### <span data-ttu-id="34aca-133">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="34aca-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="34aca-134">Microsoft. Azure. Commands. Synapse. Models. PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="34aca-134">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="34aca-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="34aca-135">OUTPUTS</span></span>

### <span data-ttu-id="34aca-136">Microsoft. Azure. Commands. Synapse. Models. PSTriggerSubscriptionOperationStatus</span><span class="sxs-lookup"><span data-stu-id="34aca-136">Microsoft.Azure.Commands.Synapse.Models.PSTriggerSubscriptionOperationStatus</span></span>

## <span data-ttu-id="34aca-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="34aca-137">NOTES</span></span>

## <span data-ttu-id="34aca-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="34aca-138">RELATED LINKS</span></span>

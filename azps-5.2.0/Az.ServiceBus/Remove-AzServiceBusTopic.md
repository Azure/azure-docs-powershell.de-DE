---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusTopic.md
ms.openlocfilehash: 75da2231dae7ea0dc587d48ca832b7631fc24986
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98369227"
---
# <span data-ttu-id="1000d-101">Remove-AzServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="1000d-101">Remove-AzServiceBusTopic</span></span>

## <span data-ttu-id="1000d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1000d-102">SYNOPSIS</span></span>
<span data-ttu-id="1000d-103">Entfernt das Thema aus dem angegebenen Service Bus-Namespace.</span><span class="sxs-lookup"><span data-stu-id="1000d-103">Removes the topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="1000d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1000d-104">SYNTAX</span></span>

### <span data-ttu-id="1000d-105">TopicPropertiesSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="1000d-105">TopicPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusTopic [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1000d-106">TopicInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="1000d-106">TopicInputObjectSet</span></span>
```
Remove-AzServiceBusTopic [-InputObject] <PSTopicAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1000d-107">TopicResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="1000d-107">TopicResourceIdSet</span></span>
```
Remove-AzServiceBusTopic [-ResourceId] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1000d-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1000d-108">DESCRIPTION</span></span>
<span data-ttu-id="1000d-109">Das **Cmdlet "Remove-AzServiceBusTopic"** entfernt das Thema aus dem angegebenen Namespace "Service Bus".</span><span class="sxs-lookup"><span data-stu-id="1000d-109">The **Remove-AzServiceBusTopic** cmdlet removes the topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="1000d-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1000d-110">EXAMPLES</span></span>

### <span data-ttu-id="1000d-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1000d-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1
```

<span data-ttu-id="1000d-112">Entfernt das Thema `SB-Topic_exampl1` aus dem `SB-Example1` Namespace.</span><span class="sxs-lookup"><span data-stu-id="1000d-112">Removes the topic `SB-Topic_exampl1` from the namespace `SB-Example1`.</span></span>

### <span data-ttu-id="1000d-113">Beispiel 2: InputObject – Verwenden der Variable:</span><span class="sxs-lookup"><span data-stu-id="1000d-113">Example 2: InputObject - Using Variable:</span></span>
```powershell
PS C:\> $inputobject = Get-AzServiceBusTopic <parmas>
PS C:\> Remove-AzServiceBusTopic -InputObject $inputobject
```

### <span data-ttu-id="1000d-114">Beispiel 3: InputObject – Verwenden der Piping:</span><span class="sxs-lookup"><span data-stu-id="1000d-114">Example 3: InputObject - Using Piping:</span></span>
```powershell
PS C:\> Get-AzServiceBusTopic <parmas> | Remove-AzServiceBusTopic
```

### <span data-ttu-id="1000d-115">Beispiel 4: ResourceId mit Variable:</span><span class="sxs-lookup"><span data-stu-id="1000d-115">Example 4: ResourceId Using Variable:</span></span>
```powershell
PS C:\> $resourceid = Get-AzServiceBusTopic <params>
PS C:\> Remove-AzServiceBusTopic -ResourceId $resourceid.Id
```

### <span data-ttu-id="1000d-116">Beispiel 5: ResourceId mithilfe des Zeichenfolgenwerts</span><span class="sxs-lookup"><span data-stu-id="1000d-116">Example 5: ResourceId Using String value</span></span>
```powershell
PS C:\> Remove-AzServiceBusTopic -ResourceId "/subscriptions/xxxx-xxxxx-xxxxxx-xxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.ServiceBus/namespaces/NamespaceName/topics/TopicName"
```

## <span data-ttu-id="1000d-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1000d-117">PARAMETERS</span></span>

### <span data-ttu-id="1000d-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1000d-118">-AsJob</span></span>
<span data-ttu-id="1000d-119">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="1000d-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1000d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1000d-120">-DefaultProfile</span></span>
<span data-ttu-id="1000d-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1000d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1000d-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1000d-122">-InputObject</span></span>
<span data-ttu-id="1000d-123">Service Bus Topic Object</span><span class="sxs-lookup"><span data-stu-id="1000d-123">Service Bus Topic Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes
Parameter Sets: TopicInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1000d-124">-Name</span><span class="sxs-lookup"><span data-stu-id="1000d-124">-Name</span></span>
<span data-ttu-id="1000d-125">Themaname</span><span class="sxs-lookup"><span data-stu-id="1000d-125">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: TopicPropertiesSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1000d-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="1000d-126">-Namespace</span></span>
<span data-ttu-id="1000d-127">Namespacename</span><span class="sxs-lookup"><span data-stu-id="1000d-127">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: TopicPropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1000d-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1000d-128">-PassThru</span></span>
<span data-ttu-id="1000d-129">Wenn Sie diese Angabe angeben, wird "true" zurückgeben, wenn der Befehl erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="1000d-129">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="1000d-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1000d-130">-ResourceGroupName</span></span>
<span data-ttu-id="1000d-131">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="1000d-131">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: TopicPropertiesSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1000d-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1000d-132">-ResourceId</span></span>
<span data-ttu-id="1000d-133">Ressourcen-ID des Dienstbusthemas</span><span class="sxs-lookup"><span data-stu-id="1000d-133">Service Bus Topic Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: TopicResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1000d-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1000d-134">-Confirm</span></span>
<span data-ttu-id="1000d-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1000d-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1000d-136">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="1000d-136">-WhatIf</span></span>
<span data-ttu-id="1000d-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1000d-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1000d-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1000d-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1000d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1000d-139">CommonParameters</span></span>
<span data-ttu-id="1000d-140">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1000d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1000d-141">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1000d-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1000d-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1000d-142">INPUTS</span></span>

### <span data-ttu-id="1000d-143">System.String</span><span class="sxs-lookup"><span data-stu-id="1000d-143">System.String</span></span>

### <span data-ttu-id="1000d-144">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="1000d-144">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="1000d-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1000d-145">OUTPUTS</span></span>

### <span data-ttu-id="1000d-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1000d-146">System.Boolean</span></span>

## <span data-ttu-id="1000d-147">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1000d-147">NOTES</span></span>

## <span data-ttu-id="1000d-148">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1000d-148">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNamespace.md
ms.openlocfilehash: 29f2b961637a398470f6455d0d2330ce5fd863a6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100167601"
---
# <span data-ttu-id="b8047-101">Remove-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="b8047-101">Remove-AzEventHubNamespace</span></span>

## <span data-ttu-id="b8047-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8047-102">SYNOPSIS</span></span>
<span data-ttu-id="b8047-103">Entfernt den angegebenen Ereignishub-Namespace.</span><span class="sxs-lookup"><span data-stu-id="b8047-103">Removes the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="b8047-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b8047-104">SYNTAX</span></span>

### <span data-ttu-id="b8047-105">NamespaceParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="b8047-105">NamespaceParameterSet (Default)</span></span>
```
Remove-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8047-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b8047-106">NamespaceInputObjectSet</span></span>
```
Remove-AzEventHubNamespace [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8047-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b8047-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzEventHubNamespace [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8047-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b8047-108">DESCRIPTION</span></span>
<span data-ttu-id="b8047-109">Das Remove-AzEventHubNamespace cmdlet entfernt und löscht den angegebenen Ereignishubs-Namespace.</span><span class="sxs-lookup"><span data-stu-id="b8047-109">The Remove-AzEventHubNamespace cmdlet removes and deletes the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="b8047-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b8047-110">EXAMPLES</span></span>

### <span data-ttu-id="b8047-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b8047-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -Name MyNamespaceName
```

<span data-ttu-id="b8047-112">Entfernt den Namespace "Event \` Hubs" "MyNamespaceName" \` in der Ressourcengruppe \` "MyResourceGroupName". \`</span><span class="sxs-lookup"><span data-stu-id="b8047-112">Removes the Event Hubs namespace \`MyNamespaceName\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="b8047-113">Beispiel 2: InputObject – Verwenden der Variable:</span><span class="sxs-lookup"><span data-stu-id="b8047-113">Example 2: InputObject - Using Variable:</span></span>
```powershell
PS C:\> $inputObject = Get-AzEventHubNamespace <params> 
PS C:\> Remove-AzEventHubNamespace -InputObject $inputObject
```

### <span data-ttu-id="b8047-114">Beispiel 3: InputObject – Verwenden der Piping:</span><span class="sxs-lookup"><span data-stu-id="b8047-114">Example 3: InputObject - Using Piping:</span></span>
```powershell
PS C:\> Get-AzEventHubNamespace <params> | Remove-AzEventHubNamespace
```

### <span data-ttu-id="b8047-115">Beispiel 4: ResourceId – Verwenden einer Variablen</span><span class="sxs-lookup"><span data-stu-id="b8047-115">Example 4: ResourceId - Using Variable</span></span>
```powershell
PS C:\> $resourceid = Get-AzEventHubNamespace <params>
PS C:\> Remove-AzEventHubNamespace -ResourceId $resourceid.Id
```

### <span data-ttu-id="b8047-116">Beispiel 5: ResourceId – Verwenden der Piping:</span><span class="sxs-lookup"><span data-stu-id="b8047-116">Example 5: ResourceId - Using Piping:</span></span>
```powershell
PS C:\> Get-AzResource -ResourceType Microsoft.EventHub/Namespaces | Remove-AzEventHubNamespace
```

### <span data-ttu-id="b8047-117">Beispiel 6: ResourceId – Verwendung der Zeichenfolge:</span><span class="sxs-lookup"><span data-stu-id="b8047-117">Example 6: ResourceId - Using String:</span></span>
```powershell
PS C:\> Remove-AzEventHubNamespace -ResourceId "/subscriptions/xxx-xxxxx-xxxxxx-xxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.EventHub/namespaces/NamespaceName"
```

## <span data-ttu-id="b8047-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b8047-118">PARAMETERS</span></span>

### <span data-ttu-id="b8047-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b8047-119">-AsJob</span></span>
<span data-ttu-id="b8047-120">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="b8047-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b8047-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8047-121">-DefaultProfile</span></span>
<span data-ttu-id="b8047-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b8047-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8047-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b8047-123">-InputObject</span></span>
<span data-ttu-id="b8047-124">EventHubs Namespace-Objekt</span><span class="sxs-lookup"><span data-stu-id="b8047-124">EventHubs Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b8047-125">-Name</span><span class="sxs-lookup"><span data-stu-id="b8047-125">-Name</span></span>
<span data-ttu-id="b8047-126">EventHub Namespacename</span><span class="sxs-lookup"><span data-stu-id="b8047-126">EventHub Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceParameterSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8047-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b8047-127">-PassThru</span></span>
<span data-ttu-id="b8047-128">Wenn Sie diese Angabe angeben, wird "true" zurückgeben, wenn der Befehl erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="b8047-128">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="b8047-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8047-129">-ResourceGroupName</span></span>
<span data-ttu-id="b8047-130">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="b8047-130">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8047-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b8047-131">-ResourceId</span></span>
<span data-ttu-id="b8047-132">EventHubs Namespace Resource Id</span><span class="sxs-lookup"><span data-stu-id="b8047-132">EventHubs Namespace Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8047-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b8047-133">-Confirm</span></span>
<span data-ttu-id="b8047-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b8047-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8047-135">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="b8047-135">-WhatIf</span></span>
<span data-ttu-id="b8047-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b8047-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8047-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b8047-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8047-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8047-138">CommonParameters</span></span>
<span data-ttu-id="b8047-139">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8047-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8047-140">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8047-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8047-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b8047-141">INPUTS</span></span>

### <span data-ttu-id="b8047-142">System.String</span><span class="sxs-lookup"><span data-stu-id="b8047-142">System.String</span></span>

### <span data-ttu-id="b8047-143">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="b8047-143">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="b8047-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b8047-144">OUTPUTS</span></span>

### <span data-ttu-id="b8047-145">System.Void</span><span class="sxs-lookup"><span data-stu-id="b8047-145">System.Void</span></span>

## <span data-ttu-id="b8047-146">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b8047-146">NOTES</span></span>

## <span data-ttu-id="b8047-147">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b8047-147">RELATED LINKS</span></span>

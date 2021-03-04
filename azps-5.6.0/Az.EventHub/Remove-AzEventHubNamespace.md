---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/remove-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNamespace.md
ms.openlocfilehash: dca9094ac66e889b5a00899f6d48d6317279c1fd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920576"
---
# <span data-ttu-id="ef2fa-101">Remove-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="ef2fa-101">Remove-AzEventHubNamespace</span></span>

## <span data-ttu-id="ef2fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef2fa-102">SYNOPSIS</span></span>
<span data-ttu-id="ef2fa-103">Entfernt den angegebenen Event Hubs-Namespace.</span><span class="sxs-lookup"><span data-stu-id="ef2fa-103">Removes the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="ef2fa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ef2fa-104">SYNTAX</span></span>

### <span data-ttu-id="ef2fa-105">NamespaceParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="ef2fa-105">NamespaceParameterSet (Default)</span></span>
```
Remove-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef2fa-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ef2fa-106">NamespaceInputObjectSet</span></span>
```
Remove-AzEventHubNamespace [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef2fa-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef2fa-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzEventHubNamespace [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef2fa-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ef2fa-108">DESCRIPTION</span></span>
<span data-ttu-id="ef2fa-109">Das Remove-AzEventHubNamespace-Cmdlet entfernt und löscht den angegebenen Event Hubs-Namespace.</span><span class="sxs-lookup"><span data-stu-id="ef2fa-109">The Remove-AzEventHubNamespace cmdlet removes and deletes the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="ef2fa-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ef2fa-110">EXAMPLES</span></span>

### <span data-ttu-id="ef2fa-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ef2fa-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -Name MyNamespaceName
```

<span data-ttu-id="ef2fa-112">Entfernt den Namespace "Ereignishubs" \` MyNamespaceName \` in der Ressourcengruppe \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="ef2fa-112">Removes the Event Hubs namespace \`MyNamespaceName\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="ef2fa-113">Beispiel 2: InputObject – Verwenden von Variablen:</span><span class="sxs-lookup"><span data-stu-id="ef2fa-113">Example 2: InputObject - Using Variable:</span></span>
```powershell
PS C:\> $inputObject = Get-AzEventHubNamespace <params> 
PS C:\> Remove-AzEventHubNamespace -InputObject $inputObject
```

### <span data-ttu-id="ef2fa-114">Beispiel 3: InputObject – Verwenden von Piping:</span><span class="sxs-lookup"><span data-stu-id="ef2fa-114">Example 3: InputObject - Using Piping:</span></span>
```powershell
PS C:\> Get-AzEventHubNamespace <params> | Remove-AzEventHubNamespace
```

### <span data-ttu-id="ef2fa-115">Beispiel 4: ResourceId – Verwenden von Variablen</span><span class="sxs-lookup"><span data-stu-id="ef2fa-115">Example 4: ResourceId - Using Variable</span></span>
```powershell
PS C:\> $resourceid = Get-AzEventHubNamespace <params>
PS C:\> Remove-AzEventHubNamespace -ResourceId $resourceid.Id
```

### <span data-ttu-id="ef2fa-116">Beispiel 5: ResourceId – Verwenden von Piping:</span><span class="sxs-lookup"><span data-stu-id="ef2fa-116">Example 5: ResourceId - Using Piping:</span></span>
```powershell
PS C:\> Get-AzResource -ResourceType Microsoft.EventHub/Namespaces | Remove-AzEventHubNamespace
```

### <span data-ttu-id="ef2fa-117">Beispiel 6: ResourceId – Verwenden der Zeichenfolge:</span><span class="sxs-lookup"><span data-stu-id="ef2fa-117">Example 6: ResourceId - Using String:</span></span>
```powershell
PS C:\> Remove-AzEventHubNamespace -ResourceId "/subscriptions/xxx-xxxxx-xxxxxx-xxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.EventHub/namespaces/NamespaceName"
```

## <span data-ttu-id="ef2fa-118">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="ef2fa-118">PARAMETERS</span></span>

### <span data-ttu-id="ef2fa-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ef2fa-119">-AsJob</span></span>
<span data-ttu-id="ef2fa-120">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="ef2fa-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ef2fa-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef2fa-121">-DefaultProfile</span></span>
<span data-ttu-id="ef2fa-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ef2fa-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef2fa-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ef2fa-123">-InputObject</span></span>
<span data-ttu-id="ef2fa-124">EventHubs-Namespaceobjekt</span><span class="sxs-lookup"><span data-stu-id="ef2fa-124">EventHubs Namespace Object</span></span>

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

### <span data-ttu-id="ef2fa-125">-Name</span><span class="sxs-lookup"><span data-stu-id="ef2fa-125">-Name</span></span>
<span data-ttu-id="ef2fa-126">Name des EventHub-Namespaces</span><span class="sxs-lookup"><span data-stu-id="ef2fa-126">EventHub Namespace Name</span></span>

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

### <span data-ttu-id="ef2fa-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ef2fa-127">-PassThru</span></span>
<span data-ttu-id="ef2fa-128">Wenn der Befehl erfolgreich war, gibt die Angabe "true" zurück.</span><span class="sxs-lookup"><span data-stu-id="ef2fa-128">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="ef2fa-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef2fa-129">-ResourceGroupName</span></span>
<span data-ttu-id="ef2fa-130">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="ef2fa-130">Resource Group Name</span></span>

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

### <span data-ttu-id="ef2fa-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ef2fa-131">-ResourceId</span></span>
<span data-ttu-id="ef2fa-132">EventHubs Namespace Resource Id</span><span class="sxs-lookup"><span data-stu-id="ef2fa-132">EventHubs Namespace Resource Id</span></span>

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

### <span data-ttu-id="ef2fa-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ef2fa-133">-Confirm</span></span>
<span data-ttu-id="ef2fa-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ef2fa-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef2fa-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef2fa-135">-WhatIf</span></span>
<span data-ttu-id="ef2fa-136">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ef2fa-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef2fa-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ef2fa-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef2fa-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef2fa-138">CommonParameters</span></span>
<span data-ttu-id="ef2fa-139">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef2fa-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef2fa-140">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef2fa-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef2fa-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ef2fa-141">INPUTS</span></span>

### <span data-ttu-id="ef2fa-142">System.String</span><span class="sxs-lookup"><span data-stu-id="ef2fa-142">System.String</span></span>

### <span data-ttu-id="ef2fa-143">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="ef2fa-143">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="ef2fa-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ef2fa-144">OUTPUTS</span></span>

### <span data-ttu-id="ef2fa-145">System.Void</span><span class="sxs-lookup"><span data-stu-id="ef2fa-145">System.Void</span></span>

## <span data-ttu-id="ef2fa-146">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="ef2fa-146">NOTES</span></span>

## <span data-ttu-id="ef2fa-147">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="ef2fa-147">RELATED LINKS</span></span>

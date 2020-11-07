---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Remove-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Remove-AzEventHubNamespace.md
ms.openlocfilehash: 38a727c2e632173befe6b5b08756d558a9c9f177
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842284"
---
# <span data-ttu-id="01295-101">Remove-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="01295-101">Remove-AzEventHubNamespace</span></span>

## <span data-ttu-id="01295-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="01295-102">SYNOPSIS</span></span>
<span data-ttu-id="01295-103">Entfernt den angegebenen Event Hubs-Namespace.</span><span class="sxs-lookup"><span data-stu-id="01295-103">Removes the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="01295-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="01295-104">SYNTAX</span></span>

### <span data-ttu-id="01295-105">NamespaceParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="01295-105">NamespaceParameterSet (Default)</span></span>
```
Remove-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01295-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="01295-106">NamespaceInputObjectSet</span></span>
```
Remove-AzEventHubNamespace [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01295-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="01295-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzEventHubNamespace [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01295-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="01295-108">DESCRIPTION</span></span>
<span data-ttu-id="01295-109">Das Remove-AzEventHubNamespace-Cmdlet entfernt den angegebenen Event Hubs-Namespace und löscht ihn.</span><span class="sxs-lookup"><span data-stu-id="01295-109">The Remove-AzEventHubNamespace cmdlet removes and deletes the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="01295-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="01295-110">EXAMPLES</span></span>

### <span data-ttu-id="01295-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="01295-111">Example 1</span></span>
```
PS C:\> Remove-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -Name MyNamespaceName
```

<span data-ttu-id="01295-112">Entfernt den Event Hubs \` -Namespace mynamespacename \` in der Ressourcengruppe \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="01295-112">Removes the Event Hubs namespace \`MyNamespaceName\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="01295-113">Beispiel 2,1-Inputobject-using-Variable:</span><span class="sxs-lookup"><span data-stu-id="01295-113">Example 2.1 - InputObject - Using Variable:</span></span>
```
PS C:\> $inputObject = Get-AzEventHubNamespace <params> 
PS C:\> Remove-AzEventHubNamespace -InputObject $inputObject
```

### <span data-ttu-id="01295-114">Beispiel 2,1-Inputobject-using Piping:</span><span class="sxs-lookup"><span data-stu-id="01295-114">Example 2.1 - InputObject - Using Piping:</span></span>
```
PS C:\> Get-AzEventHubNamespace <params> | Remove-AzEventHubNamespace
```

### <span data-ttu-id="01295-115">Beispiel 3,1-Resourcen-using-Variable</span><span class="sxs-lookup"><span data-stu-id="01295-115">Example 3.1 - ResourceId - Using Variable</span></span>
```
PS C:\> $resourceid = Get-AzEventHubNamespace <params>
PS C:\> Remove-AzEventHubNamespace -ResourceId $resourceid.Id
```

### <span data-ttu-id="01295-116">Beispiel 3,2-Resourcen-using-Piping:</span><span class="sxs-lookup"><span data-stu-id="01295-116">Example 3.2 - ResourceId - Using Piping:</span></span>
```
PS C:\> Get-AzResource -ResourceType Microsoft.EventHub/Namespaces | Remove-AzEventHubNamespace
```

### <span data-ttu-id="01295-117">Beispiel 3,3-Resourcen-using-Zeichenfolge:</span><span class="sxs-lookup"><span data-stu-id="01295-117">Example 3.3 - ResourceId - Using String:</span></span>
```
PS C:\> Remove-AzEventHubNamespace -ResourceId "/subscriptions/xxx-xxxxx-xxxxxx-xxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.EventHub/namespaces/NamespaceName"
```

## <span data-ttu-id="01295-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="01295-118">PARAMETERS</span></span>

### <span data-ttu-id="01295-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="01295-119">-AsJob</span></span>
<span data-ttu-id="01295-120">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="01295-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="01295-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01295-121">-DefaultProfile</span></span>
<span data-ttu-id="01295-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="01295-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01295-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="01295-123">-InputObject</span></span>
<span data-ttu-id="01295-124">EventHubs-Namespace Objekt</span><span class="sxs-lookup"><span data-stu-id="01295-124">EventHubs Namespace Object</span></span>

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

### <span data-ttu-id="01295-125">-Name</span><span class="sxs-lookup"><span data-stu-id="01295-125">-Name</span></span>
<span data-ttu-id="01295-126">EventHub-Namespace Name</span><span class="sxs-lookup"><span data-stu-id="01295-126">EventHub Namespace Name</span></span>

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

### <span data-ttu-id="01295-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="01295-127">-PassThru</span></span>
<span data-ttu-id="01295-128">Wenn Sie dies angeben, wird true zurückgegeben, wenn der Befehl erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="01295-128">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="01295-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01295-129">-ResourceGroupName</span></span>
<span data-ttu-id="01295-130">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="01295-130">Resource Group Name</span></span>

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

### <span data-ttu-id="01295-131">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="01295-131">-ResourceId</span></span>
<span data-ttu-id="01295-132">EventHubs-Namespace-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="01295-132">EventHubs Namespace Resource Id</span></span>

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

### <span data-ttu-id="01295-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="01295-133">-Confirm</span></span>
<span data-ttu-id="01295-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="01295-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01295-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01295-135">-WhatIf</span></span>
<span data-ttu-id="01295-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="01295-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01295-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="01295-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01295-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01295-138">CommonParameters</span></span>
<span data-ttu-id="01295-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01295-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01295-140">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01295-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01295-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="01295-141">INPUTS</span></span>

### <span data-ttu-id="01295-142">System. String</span><span class="sxs-lookup"><span data-stu-id="01295-142">System.String</span></span>

### <span data-ttu-id="01295-143">Microsoft. Azure. Commands. EventHub. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="01295-143">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="01295-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="01295-144">OUTPUTS</span></span>

### <span data-ttu-id="01295-145">System. void</span><span class="sxs-lookup"><span data-stu-id="01295-145">System.Void</span></span>

## <span data-ttu-id="01295-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="01295-146">NOTES</span></span>

## <span data-ttu-id="01295-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="01295-147">RELATED LINKS</span></span>

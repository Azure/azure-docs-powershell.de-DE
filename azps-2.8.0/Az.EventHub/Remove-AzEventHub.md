---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHub.md
ms.openlocfilehash: 1e53e1a1eb1070a9f13c9e67ea4a838358012a13
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651173"
---
# <span data-ttu-id="86f58-101">Remove-AzEventHub</span><span class="sxs-lookup"><span data-stu-id="86f58-101">Remove-AzEventHub</span></span>

## <span data-ttu-id="86f58-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="86f58-102">SYNOPSIS</span></span>
<span data-ttu-id="86f58-103">Entfernt den angegebenen Ereignis-Hub.</span><span class="sxs-lookup"><span data-stu-id="86f58-103">Removes the specified Event Hub.</span></span>

## <span data-ttu-id="86f58-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="86f58-104">SYNTAX</span></span>

### <span data-ttu-id="86f58-105">EventhubDefaultSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="86f58-105">EventhubDefaultSet (Default)</span></span>
```
Remove-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86f58-106">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="86f58-106">EventhubInputObjectSet</span></span>
```
Remove-AzEventHub [-InputObject] <PSEventHubAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86f58-107">EventhubResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="86f58-107">EventhubResourceIdParameterSet</span></span>
```
Remove-AzEventHub [-ResourceId] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86f58-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="86f58-108">DESCRIPTION</span></span>
<span data-ttu-id="86f58-109">Das Remove-AzEventHub-Cmdlet entfernt und löscht den angegebenen Ereignis-Hub aus dem angegebenen Namespace.</span><span class="sxs-lookup"><span data-stu-id="86f58-109">The Remove-AzEventHub cmdlet removes and deletes the specified Event Hub from the given namespace.</span></span>

## <span data-ttu-id="86f58-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="86f58-110">EXAMPLES</span></span>

### <span data-ttu-id="86f58-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="86f58-111">Example 1</span></span>
```
PS C:\> Remove-AzEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName
```

<span data-ttu-id="86f58-112">Entfernt den Ereignis \` -Hub \` -MyEventHubName.</span><span class="sxs-lookup"><span data-stu-id="86f58-112">Removes the Event Hub \`MyEventHubName\`.</span></span>

### <span data-ttu-id="86f58-113">Beispiel 2,1-Inputobject-using-Variable:</span><span class="sxs-lookup"><span data-stu-id="86f58-113">Example 2.1 - InputObject - Using Variable:</span></span>
```
PS C:\> $inputobject = Get-AzEventHub <params>
PS C:\> Remove-AzEventHub -InputObject $inputobject
```

### <span data-ttu-id="86f58-114">Beispiel 2,2-Inputobject mit Piping:</span><span class="sxs-lookup"><span data-stu-id="86f58-114">Example 2.2 - InputObject Using Piping:</span></span>
```
PS C:\> Get-AzEventHub <params> | Remove-AzEventHub
```

### <span data-ttu-id="86f58-115">Beispiel 3,1-Resourcen-using-Variable:</span><span class="sxs-lookup"><span data-stu-id="86f58-115">Example 3.1 - ResourceId - Using Variable:</span></span>
```
PS C:\> $resourceid = Get-AzEventHub <params>
PS C:\> Remove-AzEventHub -ResourceId $resourceid.Id
```

### <span data-ttu-id="86f58-116">Beispiel 3,1-Resourcen-using-Zeichenfolge:</span><span class="sxs-lookup"><span data-stu-id="86f58-116">Example 3.1 - ResourceId - Using string:</span></span>
```
PS C:\> Remove-AzEventHub -ResourceId "/subscriptions/xxxx-xxxxx-xxxxxx-xxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.EventHub/namespaces/NamespaceName/eventhubs/EventHubName"
```

## <span data-ttu-id="86f58-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="86f58-117">PARAMETERS</span></span>

### <span data-ttu-id="86f58-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="86f58-118">-AsJob</span></span>
<span data-ttu-id="86f58-119">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="86f58-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="86f58-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86f58-120">-DefaultProfile</span></span>
<span data-ttu-id="86f58-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="86f58-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="86f58-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="86f58-122">-InputObject</span></span>
<span data-ttu-id="86f58-123">Eventhub-Objekt</span><span class="sxs-lookup"><span data-stu-id="86f58-123">Eventhub Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes
Parameter Sets: EventhubInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="86f58-124">-Name</span><span class="sxs-lookup"><span data-stu-id="86f58-124">-Name</span></span>
<span data-ttu-id="86f58-125">EventHub Name</span><span class="sxs-lookup"><span data-stu-id="86f58-125">EventHub Name</span></span>

```yaml
Type: System.String
Parameter Sets: EventhubDefaultSet
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86f58-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="86f58-126">-Namespace</span></span>
<span data-ttu-id="86f58-127">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="86f58-127">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: EventhubDefaultSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86f58-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="86f58-128">-PassThru</span></span>
<span data-ttu-id="86f58-129">Wenn Sie dies angeben, wird true zurückgegeben, wenn der Befehl erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="86f58-129">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="86f58-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86f58-130">-ResourceGroupName</span></span>
<span data-ttu-id="86f58-131">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="86f58-131">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: EventhubDefaultSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86f58-132">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="86f58-132">-ResourceId</span></span>
<span data-ttu-id="86f58-133">Eventhub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="86f58-133">Eventhub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: EventhubResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86f58-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="86f58-134">-Confirm</span></span>
<span data-ttu-id="86f58-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="86f58-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86f58-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86f58-136">-WhatIf</span></span>
<span data-ttu-id="86f58-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="86f58-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86f58-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="86f58-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86f58-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86f58-139">CommonParameters</span></span>
<span data-ttu-id="86f58-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86f58-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86f58-141">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86f58-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86f58-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="86f58-142">INPUTS</span></span>

### <span data-ttu-id="86f58-143">System. String</span><span class="sxs-lookup"><span data-stu-id="86f58-143">System.String</span></span>

### <span data-ttu-id="86f58-144">Microsoft. Azure. Commands. EventHub. Models. PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="86f58-144">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="86f58-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="86f58-145">OUTPUTS</span></span>

### <span data-ttu-id="86f58-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="86f58-146">System.Boolean</span></span>

## <span data-ttu-id="86f58-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="86f58-147">NOTES</span></span>

## <span data-ttu-id="86f58-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="86f58-148">RELATED LINKS</span></span>

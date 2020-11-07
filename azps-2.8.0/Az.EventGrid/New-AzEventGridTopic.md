---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopic.md
ms.openlocfilehash: 25882d3fe897c77df864d429cfc3cd9d31197916
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651223"
---
# <span data-ttu-id="6c807-101">New-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="6c807-101">New-AzEventGridTopic</span></span>

## <span data-ttu-id="6c807-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6c807-102">SYNOPSIS</span></span>
<span data-ttu-id="6c807-103">Erstellt ein neues Azure-Ereignis Raster Thema.</span><span class="sxs-lookup"><span data-stu-id="6c807-103">Creates a new Azure Event Grid Topic.</span></span>

## <span data-ttu-id="6c807-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6c807-104">SYNTAX</span></span>

```
New-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c807-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6c807-105">DESCRIPTION</span></span>
<span data-ttu-id="6c807-106">Erstellt ein neues Azure-Ereignis Raster Thema.</span><span class="sxs-lookup"><span data-stu-id="6c807-106">Creates a new Azure Event Grid Topic.</span></span> <span data-ttu-id="6c807-107">Nach dem Erstellen des Themas kann eine Anwendung Ereignisse im Themen Endpunkt veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="6c807-107">Once the topic is created, an application can publish events to the topic endpoint.</span></span>

## <span data-ttu-id="6c807-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6c807-108">EXAMPLES</span></span>

### <span data-ttu-id="6c807-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6c807-109">Example 1</span></span>
```powershell
PS C:\> New-AzEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1 -Location westus2
```

<span data-ttu-id="6c807-110">Erstellt ein Ereignis Raster Thema \` THEMA1 hat \` im angegebenen geografischen \` Standort \` westus2, in der Ressourcengruppe \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="6c807-110">Creates an Event Grid topic \`Topic1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="6c807-111">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="6c807-111">Example 2</span></span>
```powershell
PS C:\> New-AzEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1 -Location westus2 -Tag @{ Department="Finance"; Environment="Test" }
```

<span data-ttu-id="6c807-112">Erstellt ein Ereignis Raster Thema \` THEMA1 hat am \` angegebenen geografischen Standort \` westus2 \` , in der Ressourcengruppe \` MyResourceGroupName \` mit den angegebenen Tags "Department" und "Environment".</span><span class="sxs-lookup"><span data-stu-id="6c807-112">Creates an Event Grid topic \`Topic1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\` with the specified tags "Department" and "Environment".</span></span>

## <span data-ttu-id="6c807-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="6c807-113">PARAMETERS</span></span>

### <span data-ttu-id="6c807-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c807-114">-DefaultProfile</span></span>
<span data-ttu-id="6c807-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="6c807-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6c807-116">-Standort</span><span class="sxs-lookup"><span data-stu-id="6c807-116">-Location</span></span>
<span data-ttu-id="6c807-117">Der Speicherort des Themas</span><span class="sxs-lookup"><span data-stu-id="6c807-117">The location of the topic</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c807-118">-Name</span><span class="sxs-lookup"><span data-stu-id="6c807-118">-Name</span></span>
<span data-ttu-id="6c807-119">Der Name des Themas.</span><span class="sxs-lookup"><span data-stu-id="6c807-119">The name of the topic.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c807-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c807-120">-ResourceGroupName</span></span>
<span data-ttu-id="6c807-121">Die Ressourcengruppe, in der das Thema erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="6c807-121">The resource group in which the topic should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c807-122">-Tag</span><span class="sxs-lookup"><span data-stu-id="6c807-122">-Tag</span></span>
<span data-ttu-id="6c807-123">Hashtables, die Ressourcen Tags darstellen.</span><span class="sxs-lookup"><span data-stu-id="6c807-123">Hashtables which represents resource Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c807-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6c807-124">-Confirm</span></span>
<span data-ttu-id="6c807-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6c807-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c807-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c807-126">-WhatIf</span></span>
<span data-ttu-id="6c807-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6c807-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c807-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6c807-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c807-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c807-129">CommonParameters</span></span>
<span data-ttu-id="6c807-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c807-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c807-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c807-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c807-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6c807-132">INPUTS</span></span>

### <span data-ttu-id="6c807-133">System. String</span><span class="sxs-lookup"><span data-stu-id="6c807-133">System.String</span></span>

### <span data-ttu-id="6c807-134">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="6c807-134">System.Collections.Hashtable</span></span>

## <span data-ttu-id="6c807-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6c807-135">OUTPUTS</span></span>

### <span data-ttu-id="6c807-136">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="6c807-136">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="6c807-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="6c807-137">NOTES</span></span>

## <span data-ttu-id="6c807-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6c807-138">RELATED LINKS</span></span>

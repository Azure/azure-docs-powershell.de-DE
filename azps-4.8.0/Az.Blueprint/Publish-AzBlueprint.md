---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/publish-azblueprint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Publish-AzBlueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Publish-AzBlueprint.md
ms.openlocfilehash: 32b59902bca68496c3a6c9e1656ac618824b9f38
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008102"
---
# <span data-ttu-id="1bf4c-101">Publish-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="1bf4c-101">Publish-AzBlueprint</span></span>

## <span data-ttu-id="1bf4c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1bf4c-102">SYNOPSIS</span></span>
<span data-ttu-id="1bf4c-103">Veröffentlichen einer neuen Version eines Blueprints</span><span class="sxs-lookup"><span data-stu-id="1bf4c-103">Publish a new version of a blueprint.</span></span>

## <span data-ttu-id="1bf4c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1bf4c-104">SYNTAX</span></span>

```
Publish-AzBlueprint -Version <String> [-ChangeNote <String>] -Blueprint <PSBlueprint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1bf4c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1bf4c-105">DESCRIPTION</span></span>
<span data-ttu-id="1bf4c-106">Veröffentlichen einer neuen Version einer Blueprint-Definition</span><span class="sxs-lookup"><span data-stu-id="1bf4c-106">Publish a new version of a blueprint definition.</span></span>

## <span data-ttu-id="1bf4c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1bf4c-107">EXAMPLES</span></span>

### <span data-ttu-id="1bf4c-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1bf4c-108">Example 1</span></span>
```powershell
PS C:\> Publish-AzBlueprint -Blueprint $bp -Version 1.0 

Name           : SimpleBlueprint
Id             : /subscriptions/{subscriptionId}/providers/Microsoft.Blueprint/blueprints/SimpleBlueprint/versions/1.0
SubscriptionId : 00000000-1111-0000-1111-000000000000
Version        : 1.0
Description    : My simple blueprint
TimeCreated    : 2019-05-30
TargetScope    : Subscription
Parameters     : {[tagName, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue], [tagValue, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue]}
ResourceGroups : {storageRG}
```

<span data-ttu-id="1bf4c-109">Veröffentlichen einer neuen Version einer Blueprint-Definition</span><span class="sxs-lookup"><span data-stu-id="1bf4c-109">Publish a new version of a blueprint definition.</span></span>

## <span data-ttu-id="1bf4c-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="1bf4c-110">PARAMETERS</span></span>

### <span data-ttu-id="1bf4c-111">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="1bf4c-111">-Blueprint</span></span>
<span data-ttu-id="1bf4c-112">Blueprint-Objekt</span><span class="sxs-lookup"><span data-stu-id="1bf4c-112">Blueprint object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1bf4c-113">-ChangeNote</span><span class="sxs-lookup"><span data-stu-id="1bf4c-113">-ChangeNote</span></span>
<span data-ttu-id="1bf4c-114">Hinweise zum Beschreiben des Inhalts dieser Blueprint-Version.</span><span class="sxs-lookup"><span data-stu-id="1bf4c-114">Notes to describe the contents of this blueprint version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bf4c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bf4c-115">-DefaultProfile</span></span>
<span data-ttu-id="1bf4c-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1bf4c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1bf4c-117">-Version</span><span class="sxs-lookup"><span data-stu-id="1bf4c-117">-Version</span></span>
<span data-ttu-id="1bf4c-118">Version für die Blueprint-Definition</span><span class="sxs-lookup"><span data-stu-id="1bf4c-118">Version for the blueprint definition.</span></span>

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

### <span data-ttu-id="1bf4c-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1bf4c-119">-Confirm</span></span>
<span data-ttu-id="1bf4c-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1bf4c-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1bf4c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1bf4c-121">-WhatIf</span></span>
<span data-ttu-id="1bf4c-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1bf4c-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1bf4c-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1bf4c-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1bf4c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bf4c-124">CommonParameters</span></span>
<span data-ttu-id="1bf4c-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1bf4c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bf4c-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1bf4c-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bf4c-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1bf4c-127">INPUTS</span></span>

### <span data-ttu-id="1bf4c-128">System. String</span><span class="sxs-lookup"><span data-stu-id="1bf4c-128">System.String</span></span>

### <span data-ttu-id="1bf4c-129">Microsoft. Azure. Commands. Blueprint. Models. PSBlueprint</span><span class="sxs-lookup"><span data-stu-id="1bf4c-129">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint</span></span>

## <span data-ttu-id="1bf4c-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1bf4c-130">OUTPUTS</span></span>

### <span data-ttu-id="1bf4c-131">Microsoft. Azure. Commands. Blueprint. Models. PSPublishedBlueprint</span><span class="sxs-lookup"><span data-stu-id="1bf4c-131">Microsoft.Azure.Commands.Blueprint.Models.PSPublishedBlueprint</span></span>

## <span data-ttu-id="1bf4c-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="1bf4c-132">NOTES</span></span>

## <span data-ttu-id="1bf4c-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1bf4c-133">RELATED LINKS</span></span>

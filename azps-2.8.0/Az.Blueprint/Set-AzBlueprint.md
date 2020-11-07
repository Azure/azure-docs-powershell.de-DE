---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/set-azblueprint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprint.md
ms.openlocfilehash: 7366e263f6106d2d332daab95f029d07c824aa90
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93652334"
---
# <span data-ttu-id="b8747-101">Set-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="b8747-101">Set-AzBlueprint</span></span>

## <span data-ttu-id="b8747-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b8747-102">SYNOPSIS</span></span>
<span data-ttu-id="b8747-103">Aktualisieren einer Blueprint-Definition</span><span class="sxs-lookup"><span data-stu-id="b8747-103">Update a blueprint definition.</span></span>

## <span data-ttu-id="b8747-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b8747-104">SYNTAX</span></span>

### <span data-ttu-id="b8747-105">UpdateBlueprintBySubscription (Standard)</span><span class="sxs-lookup"><span data-stu-id="b8747-105">UpdateBlueprintBySubscription (Default)</span></span>
```
Set-AzBlueprint -Name <String> [-SubscriptionId <String>] -BlueprintFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8747-106">UpdateBlueprintByManagementGroup</span><span class="sxs-lookup"><span data-stu-id="b8747-106">UpdateBlueprintByManagementGroup</span></span>
```
Set-AzBlueprint -Name <String> -ManagementGroupId <String> -BlueprintFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8747-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b8747-107">DESCRIPTION</span></span>
<span data-ttu-id="b8747-108">Aktualisieren Sie eine Blueprint-Definition, und speichern Sie Sie in der angegebenen Abonnement-oder Verwaltungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="b8747-108">Update a blueprint definition and save it within the specified subscription or management group.</span></span>

## <span data-ttu-id="b8747-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b8747-109">EXAMPLES</span></span>

### <span data-ttu-id="b8747-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b8747-110">Example 1</span></span>
```powershell
PS C:\> Set-AzBlueprint -Name MyBlueprint -SubscriptionId 00000000-1111-0000-1111-000000000000 -BlueprintFile C:\Blueprint.json

Name              : SimpleBlueprint
Id                : /providers/Microsoft.Management/managementGroups/{mgId}/providers/Microsoft.Blueprint/blueprints/SimpleBlueprint
ManagementGroupId : myManagementGroupId
Versions          : 
Description       : test
TimeCreated       : 2019-05-12
TargetScope       : Subscription
Parameters        : {enforcetaganditsvalue_tagName, enforcetaganditsvalue_tagValue}
ResourceGroups    : {AppNetworkRG}
```

<span data-ttu-id="b8747-111">Aktualisieren einer Blueprint-Definition mit neuen Parametern</span><span class="sxs-lookup"><span data-stu-id="b8747-111">Update a blueprint definition with new parameters.</span></span>

## <span data-ttu-id="b8747-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="b8747-112">PARAMETERS</span></span>

### <span data-ttu-id="b8747-113">-Blueprintdatei</span><span class="sxs-lookup"><span data-stu-id="b8747-113">-BlueprintFile</span></span>
<span data-ttu-id="b8747-114">Pfad zu einer Blueprint-JSON-Datei auf dem Datenträger.</span><span class="sxs-lookup"><span data-stu-id="b8747-114">Path to a Blueprint JSON file on disk.</span></span>

```yaml
Type: String
Parameter Sets: CreateBlueprintBySubscription, CreateBlueprintByManagementGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8747-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8747-115">-DefaultProfile</span></span>
<span data-ttu-id="b8747-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b8747-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8747-117">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="b8747-117">-ManagementGroupId</span></span>
<span data-ttu-id="b8747-118">Verwaltungsgruppen-ID, in der die Blueprint-Definition steht oder gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="b8747-118">Management Group Id where the blueprint definition is or will be saved.</span></span>

```yaml
Type: String
Parameter Sets: CreateBlueprintByManagementGroup, ManagementGroupScope, ByManagementGroupAndName, ByManagementGroupNameAndVersion, ByManagementGroupNameAndLatestPublished
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ImportBlueprint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8747-119">-Name</span><span class="sxs-lookup"><span data-stu-id="b8747-119">-Name</span></span>
<span data-ttu-id="b8747-120">Blueprint-Definitionsname</span><span class="sxs-lookup"><span data-stu-id="b8747-120">Blueprint definition name.</span></span>

```yaml
Type: String
Parameter Sets: CreateBlueprintBySubscription, CreateBlueprintByManagementGroup, ImportBlueprint
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8747-121">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="b8747-121">-SubscriptionId</span></span>
<span data-ttu-id="b8747-122">Die Abonnement-ID, in der die Blueprint-Definition fest steht oder gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="b8747-122">Subscription Id where the blueprint definition is or will be saved.</span></span>

```yaml
Type: String
Parameter Sets: CreateBlueprintBySubscription, ImportBlueprint, SubscriptionScope, BySubscriptionAndName, BySubscriptionNameAndVersion, BySubscriptionNameAndLatestPublished
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8747-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b8747-123">-Confirm</span></span>
<span data-ttu-id="b8747-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b8747-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8747-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8747-125">-WhatIf</span></span>
<span data-ttu-id="b8747-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b8747-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8747-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b8747-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8747-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8747-128">CommonParameters</span></span>
<span data-ttu-id="b8747-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8747-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="b8747-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8747-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8747-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b8747-131">INPUTS</span></span>

### <span data-ttu-id="b8747-132">System. String</span><span class="sxs-lookup"><span data-stu-id="b8747-132">System.String</span></span>

## <span data-ttu-id="b8747-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b8747-133">OUTPUTS</span></span>

### <span data-ttu-id="b8747-134">Microsoft. Azure. Commands. Blueprint. Models. PSBlueprint</span><span class="sxs-lookup"><span data-stu-id="b8747-134">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint</span></span>

## <span data-ttu-id="b8747-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="b8747-135">NOTES</span></span>

## <span data-ttu-id="b8747-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b8747-136">RELATED LINKS</span></span>

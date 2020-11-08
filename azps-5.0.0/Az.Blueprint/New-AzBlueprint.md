---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/new-azblueprint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprint.md
ms.openlocfilehash: 790a74ef5a296dbc90e9c1db16678b8c1bacf071
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176311"
---
# <span data-ttu-id="7b177-101">New-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="7b177-101">New-AzBlueprint</span></span>

## <span data-ttu-id="7b177-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7b177-102">SYNOPSIS</span></span>
<span data-ttu-id="7b177-103">Erstellen Sie eine neue Blueprint-Definition, und speichern Sie Sie in der angegebenen Abonnement-oder Verwaltungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="7b177-103">Create a new blueprint definition and save it within the specified subscription or management group.</span></span>

## <span data-ttu-id="7b177-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7b177-104">SYNTAX</span></span>

### <span data-ttu-id="7b177-105">CreateBlueprintBySubscription (Standard)</span><span class="sxs-lookup"><span data-stu-id="7b177-105">CreateBlueprintBySubscription (Default)</span></span>
```
New-AzBlueprint -Name <String> [-SubscriptionId <String>] -BlueprintFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b177-106">CreateBlueprintByManagementGroup</span><span class="sxs-lookup"><span data-stu-id="7b177-106">CreateBlueprintByManagementGroup</span></span>
```
New-AzBlueprint -Name <String> -ManagementGroupId <String> -BlueprintFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b177-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7b177-107">DESCRIPTION</span></span>
<span data-ttu-id="7b177-108">Erstellen Sie eine neue Blueprint-Definition.</span><span class="sxs-lookup"><span data-stu-id="7b177-108">Create a new blueprint definition.</span></span> 

## <span data-ttu-id="7b177-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7b177-109">EXAMPLES</span></span>

### <span data-ttu-id="7b177-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7b177-110">Example 1</span></span>
```powershell
PS C:\> New-AzBlueprint -Name MyNewBlueprint -SubscriptionId 00000000-1111-0000-1111-000000000000 -BlueprintFile C:\Blueprint.json

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

<span data-ttu-id="7b177-111">Erstellen Sie eine neue Blueprint-Definition innerhalb des angegebenen Abonnements.</span><span class="sxs-lookup"><span data-stu-id="7b177-111">Create a new blueprint definition within the specified subscription.</span></span>

## <span data-ttu-id="7b177-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="7b177-112">PARAMETERS</span></span>

### <span data-ttu-id="7b177-113">-Blueprintdatei</span><span class="sxs-lookup"><span data-stu-id="7b177-113">-BlueprintFile</span></span>
<span data-ttu-id="7b177-114">Pfad zu einer Blueprint-JSON-Datei auf dem Datenträger.</span><span class="sxs-lookup"><span data-stu-id="7b177-114">Path to a Blueprint JSON file on disk.</span></span>

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

### <span data-ttu-id="7b177-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b177-115">-DefaultProfile</span></span>
<span data-ttu-id="7b177-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7b177-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b177-117">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="7b177-117">-ManagementGroupId</span></span>
<span data-ttu-id="7b177-118">Verwaltungsgruppen-ID, in der die Blueprint-Definition steht oder gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="7b177-118">Management Group Id where the blueprint definition is or will be saved.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateBlueprintByManagementGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b177-119">-Name</span><span class="sxs-lookup"><span data-stu-id="7b177-119">-Name</span></span>
<span data-ttu-id="7b177-120">Blueprint-Definitionsname</span><span class="sxs-lookup"><span data-stu-id="7b177-120">Blueprint definition name.</span></span>

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

### <span data-ttu-id="7b177-121">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="7b177-121">-SubscriptionId</span></span>
<span data-ttu-id="7b177-122">Die Abonnement-ID, in der die Blueprint-Definition fest steht oder gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="7b177-122">Subscription Id where the blueprint definition is or will be saved.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateBlueprintBySubscription
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b177-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7b177-123">-Confirm</span></span>
<span data-ttu-id="7b177-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7b177-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b177-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b177-125">-WhatIf</span></span>
<span data-ttu-id="7b177-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7b177-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b177-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7b177-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b177-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b177-128">CommonParameters</span></span>
<span data-ttu-id="7b177-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b177-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b177-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7b177-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b177-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7b177-131">INPUTS</span></span>

### <span data-ttu-id="7b177-132">System. String</span><span class="sxs-lookup"><span data-stu-id="7b177-132">System.String</span></span>

## <span data-ttu-id="7b177-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7b177-133">OUTPUTS</span></span>

### <span data-ttu-id="7b177-134">Microsoft. Azure. Commands. Blueprint. Models. PSBlueprint</span><span class="sxs-lookup"><span data-stu-id="7b177-134">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint</span></span>

## <span data-ttu-id="7b177-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="7b177-135">NOTES</span></span>

## <span data-ttu-id="7b177-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7b177-136">RELATED LINKS</span></span>

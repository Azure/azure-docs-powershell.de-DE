---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/remove-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Remove-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Remove-AzBlueprintAssignment.md
ms.openlocfilehash: 34f8b99ef4c8958415780fecb98c291d2845209d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995691"
---
# <span data-ttu-id="fda6c-101">Remove-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="fda6c-101">Remove-AzBlueprintAssignment</span></span>

## <span data-ttu-id="fda6c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fda6c-102">SYNOPSIS</span></span>
<span data-ttu-id="fda6c-103">Entfernen einer Blueprint-Zuordnung aus einem Abonnement</span><span class="sxs-lookup"><span data-stu-id="fda6c-103">Remove a blueprint assignment from a subscription.</span></span>

## <span data-ttu-id="fda6c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fda6c-104">SYNTAX</span></span>

### <span data-ttu-id="fda6c-105">DeleteBlueprintAssignmentByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="fda6c-105">DeleteBlueprintAssignmentByName (Default)</span></span>
```
Remove-AzBlueprintAssignment [[-SubscriptionId] <String>] [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fda6c-106">DeleteBlueprintAssignmentByObject</span><span class="sxs-lookup"><span data-stu-id="fda6c-106">DeleteBlueprintAssignmentByObject</span></span>
```
Remove-AzBlueprintAssignment [[-SubscriptionId] <String>] [-InputObject] <PSBlueprintAssignment> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fda6c-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fda6c-107">DESCRIPTION</span></span>
<span data-ttu-id="fda6c-108">Entfernen eines Blueprints, der einem Abonnement zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="fda6c-108">Remove a blueprint that has been assigned to a subscription.</span></span>

## <span data-ttu-id="fda6c-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fda6c-109">EXAMPLES</span></span>

### <span data-ttu-id="fda6c-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fda6c-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzBlueprintAssignment -Name "myAssignment" -Subscription "00000000-1111-0000-1111-000000000000" -Confirm
```

<span data-ttu-id="fda6c-111">Entfernen Sie die durch den Namen angegebene Blueprint-Aufgabe aus dem angegebenen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fda6c-111">Remove the blueprint assignment specified by name from the specified subscription.</span></span> <span data-ttu-id="fda6c-112">Das Cmdlet fordert zur Bestätigung auf, bevor der Befehl ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fda6c-112">The cmdlet will prompt for confirmation before executing the command.</span></span>

## <span data-ttu-id="fda6c-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="fda6c-113">PARAMETERS</span></span>

### <span data-ttu-id="fda6c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fda6c-114">-DefaultProfile</span></span>
<span data-ttu-id="fda6c-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fda6c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fda6c-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="fda6c-116">-InputObject</span></span>
<span data-ttu-id="fda6c-117">Blueprint-Zuordnungsobjekt</span><span class="sxs-lookup"><span data-stu-id="fda6c-117">Blueprint assignment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment
Parameter Sets: DeleteBlueprintAssignmentByObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fda6c-118">-Name</span><span class="sxs-lookup"><span data-stu-id="fda6c-118">-Name</span></span>
<span data-ttu-id="fda6c-119">Blueprint-Zuordnungsname</span><span class="sxs-lookup"><span data-stu-id="fda6c-119">Blueprint assignment name.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteBlueprintAssignmentByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fda6c-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fda6c-120">-PassThru</span></span>
<span data-ttu-id="fda6c-121">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="fda6c-121">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="fda6c-122">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="fda6c-122">-SubscriptionId</span></span>
<span data-ttu-id="fda6c-123">Die Abonnement-ID, in der die Blueprint-Aufgabe bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="fda6c-123">Subscription Id the blueprint assignment is deployed to.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteBlueprintAssignmentByName
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DeleteBlueprintAssignmentByObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fda6c-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fda6c-124">-Confirm</span></span>
<span data-ttu-id="fda6c-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fda6c-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fda6c-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fda6c-126">-WhatIf</span></span>
<span data-ttu-id="fda6c-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fda6c-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fda6c-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fda6c-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fda6c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fda6c-129">CommonParameters</span></span>
<span data-ttu-id="fda6c-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fda6c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fda6c-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fda6c-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fda6c-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fda6c-132">INPUTS</span></span>

### <span data-ttu-id="fda6c-133">System. String</span><span class="sxs-lookup"><span data-stu-id="fda6c-133">System.String</span></span>

### <span data-ttu-id="fda6c-134">Microsoft. Azure. Commands. Blueprint. Models. PSBlueprintAssignment []</span><span class="sxs-lookup"><span data-stu-id="fda6c-134">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment[]</span></span>

## <span data-ttu-id="fda6c-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fda6c-135">OUTPUTS</span></span>

### <span data-ttu-id="fda6c-136">System. Object</span><span class="sxs-lookup"><span data-stu-id="fda6c-136">System.Object</span></span>
## <span data-ttu-id="fda6c-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="fda6c-137">NOTES</span></span>

## <span data-ttu-id="fda6c-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fda6c-138">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/import-azblueprintwithartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Import-AzBlueprintWithArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Import-AzBlueprintWithArtifact.md
ms.openlocfilehash: 43877ecb7fe7e90f0619a26a54eea534ac1390b3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176316"
---
# <span data-ttu-id="c3678-101">Import-AzBlueprintWithArtifact</span><span class="sxs-lookup"><span data-stu-id="c3678-101">Import-AzBlueprintWithArtifact</span></span>

## <span data-ttu-id="c3678-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c3678-102">SYNOPSIS</span></span>
<span data-ttu-id="c3678-103">Importieren Sie eine Blueprint-Datei im JSON-Format in ein Blueprint-Objekt, und speichern Sie Sie in der angegebenen Abonnement-oder Verwaltungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="c3678-103">Import a blueprint file in JSON format to a blueprint object and save it within the specified subscription or management group.</span></span>

## <span data-ttu-id="c3678-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c3678-104">SYNTAX</span></span>

```
Import-AzBlueprintWithArtifact -Name <String> [-SubscriptionId <String>] [-ManagementGroupId <String>]
 -InputPath <String> [-IncludeSubFolders] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3678-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c3678-105">DESCRIPTION</span></span>
<span data-ttu-id="c3678-106">Importieren Sie eine Blueprint-Definition mit ihren Artefakten.</span><span class="sxs-lookup"><span data-stu-id="c3678-106">Import a blueprint definition with its artifacts.</span></span> 

## <span data-ttu-id="c3678-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c3678-107">EXAMPLES</span></span>

### <span data-ttu-id="c3678-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c3678-108">Example 1</span></span>
```powershell
PS C:\> Import-AzBlueprintWithArtifact -Name MySimpleBlueprint -SubscriptionId 00000000-1111-0000-1111-000000000000 -InputPath  C:\Blueprints\SimpleBlueprint
```

<span data-ttu-id="c3678-109">Importieren Sie eine Blueprint-Definition mit ihren Artefakten, und speichern Sie Sie in einem Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c3678-109">Import a blueprint definition with its artifacts and save within a subscription.</span></span>

## <span data-ttu-id="c3678-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="c3678-110">PARAMETERS</span></span>

### <span data-ttu-id="c3678-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3678-111">-DefaultProfile</span></span>
<span data-ttu-id="c3678-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c3678-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3678-113">-Force</span><span class="sxs-lookup"><span data-stu-id="c3678-113">-Force</span></span>
<span data-ttu-id="c3678-114">Wenn die Ausführung auf "true" festgelegt ist, werden Sie nicht aufgefordert, eine Bestätigung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c3678-114">When set to true, execution will not ask for a confirmation.</span></span>

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

### <span data-ttu-id="c3678-115">-IncludeSubFolders</span><span class="sxs-lookup"><span data-stu-id="c3678-115">-IncludeSubFolders</span></span>
<span data-ttu-id="c3678-116">Wenn Sie auf "true" festgelegt ist, wird das Artefakt in den Unterordnern eingefügt.</span><span class="sxs-lookup"><span data-stu-id="c3678-116">When set to true, artifact in the subfolders will be included.</span></span>

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

### <span data-ttu-id="c3678-117">-InputPath</span><span class="sxs-lookup"><span data-stu-id="c3678-117">-InputPath</span></span>
<span data-ttu-id="c3678-118">Pfad zu einer Blueprint-JSON-Datei auf dem Datenträger.</span><span class="sxs-lookup"><span data-stu-id="c3678-118">Path to a Blueprint JSON file on disk.</span></span>

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

### <span data-ttu-id="c3678-119">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="c3678-119">-ManagementGroupId</span></span>
<span data-ttu-id="c3678-120">Verwaltungsgruppen-ID, in der die Blueprint-Definition steht oder gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="c3678-120">Management Group Id where the blueprint definition is or will be saved.</span></span>

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

### <span data-ttu-id="c3678-121">-Name</span><span class="sxs-lookup"><span data-stu-id="c3678-121">-Name</span></span>
<span data-ttu-id="c3678-122">Blueprint-Definitionsname</span><span class="sxs-lookup"><span data-stu-id="c3678-122">Blueprint definition name.</span></span>

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

### <span data-ttu-id="c3678-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c3678-123">-PassThru</span></span>
<span data-ttu-id="c3678-124">Wenn festgesetzt, gibt das Cmdlet ein Objekt zurück, das die importierte Blueprint-Definition darstellt.</span><span class="sxs-lookup"><span data-stu-id="c3678-124">When set, the cmdlet will return an object representing the imported blueprint definition.</span></span> <span data-ttu-id="c3678-125">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="c3678-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c3678-126">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="c3678-126">-SubscriptionId</span></span>
<span data-ttu-id="c3678-127">Die Abonnement-ID, in der die Blueprint-Definition fest steht oder gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="c3678-127">Subscription Id where the blueprint definition is or will be saved.</span></span>

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

### <span data-ttu-id="c3678-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c3678-128">-Confirm</span></span>
<span data-ttu-id="c3678-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c3678-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3678-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3678-130">-WhatIf</span></span>
<span data-ttu-id="c3678-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c3678-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c3678-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c3678-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3678-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3678-133">CommonParameters</span></span>
<span data-ttu-id="c3678-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3678-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3678-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c3678-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3678-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c3678-136">INPUTS</span></span>

### <span data-ttu-id="c3678-137">System. String</span><span class="sxs-lookup"><span data-stu-id="c3678-137">System.String</span></span>

## <span data-ttu-id="c3678-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c3678-138">OUTPUTS</span></span>

### <span data-ttu-id="c3678-139">System. String</span><span class="sxs-lookup"><span data-stu-id="c3678-139">System.String</span></span>

## <span data-ttu-id="c3678-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="c3678-140">NOTES</span></span>

## <span data-ttu-id="c3678-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c3678-141">RELATED LINKS</span></span>

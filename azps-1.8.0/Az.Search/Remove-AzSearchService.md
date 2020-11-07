---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/remove-azsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchService.md
ms.openlocfilehash: 245cbce2516dcb26502313bcac35dd35b957f94d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659478"
---
# <span data-ttu-id="449a9-101">Remove-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="449a9-101">Remove-AzSearchService</span></span>

## <span data-ttu-id="449a9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="449a9-102">SYNOPSIS</span></span>
<span data-ttu-id="449a9-103">Entfernen eines Azure-Suchdiensts</span><span class="sxs-lookup"><span data-stu-id="449a9-103">Remove an Azure Search service.</span></span>

## <span data-ttu-id="449a9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="449a9-104">SYNTAX</span></span>

### <span data-ttu-id="449a9-105">ResourceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="449a9-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzSearchService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="449a9-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="449a9-106">InputObjectParameterSet</span></span>
```
Remove-AzSearchService [-InputObject] <PSSearchService> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="449a9-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="449a9-107">ResourceIdParameterSet</span></span>
```
Remove-AzSearchService [-ResourceId] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="449a9-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="449a9-108">DESCRIPTION</span></span>
<span data-ttu-id="449a9-109">Das Cmdlet **Remove-AzSearchService** entfernt einen Azure-Suchdienst mit dem angegebenen Parametern.</span><span class="sxs-lookup"><span data-stu-id="449a9-109">The **Remove-AzSearchService** cmdlet removes an Azure Search service with specified paramters.</span></span>

## <span data-ttu-id="449a9-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="449a9-110">EXAMPLES</span></span>

### <span data-ttu-id="449a9-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="449a9-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSearchService -ResourceGroupName "TestAzureSearchPsGroup" -Name "pstestazuresearch01"

Confirm
Are you sure you want to remove Search Service 'pstestazuresearch01'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
PS C:\>
```

<span data-ttu-id="449a9-112">Im Beispiel wird ein Azure-Suchdienst entfernt.</span><span class="sxs-lookup"><span data-stu-id="449a9-112">The example removes an Azure Search service.</span></span>

## <span data-ttu-id="449a9-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="449a9-113">PARAMETERS</span></span>

### <span data-ttu-id="449a9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="449a9-114">-DefaultProfile</span></span>
<span data-ttu-id="449a9-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="449a9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="449a9-116">-Force</span><span class="sxs-lookup"><span data-stu-id="449a9-116">-Force</span></span>
<span data-ttu-id="449a9-117">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="449a9-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="449a9-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="449a9-118">-InputObject</span></span>
<span data-ttu-id="449a9-119">Suchdienst Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="449a9-119">Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="449a9-120">-Name</span><span class="sxs-lookup"><span data-stu-id="449a9-120">-Name</span></span>
<span data-ttu-id="449a9-121">Name des Suchdiensts</span><span class="sxs-lookup"><span data-stu-id="449a9-121">Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="449a9-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="449a9-122">-PassThru</span></span>
<span data-ttu-id="449a9-123">Dieses Cmdlet gibt standardmäßig kein Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="449a9-123">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="449a9-124">Wenn dieser Schalter angegeben wird, wird true zurückgegeben, wenn er erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="449a9-124">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="449a9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="449a9-125">-ResourceGroupName</span></span>
<span data-ttu-id="449a9-126">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="449a9-126">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="449a9-127">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="449a9-127">-ResourceId</span></span>
<span data-ttu-id="449a9-128">Ressourcen-ID des Suchdiensts.</span><span class="sxs-lookup"><span data-stu-id="449a9-128">Search Service Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="449a9-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="449a9-129">-Confirm</span></span>
<span data-ttu-id="449a9-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="449a9-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="449a9-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="449a9-131">-WhatIf</span></span>
<span data-ttu-id="449a9-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="449a9-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="449a9-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="449a9-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="449a9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="449a9-134">CommonParameters</span></span>
<span data-ttu-id="449a9-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="449a9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="449a9-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="449a9-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="449a9-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="449a9-137">INPUTS</span></span>

### <span data-ttu-id="449a9-138">Microsoft. Azure. Commands. Management. search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="449a9-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="449a9-139">System. String</span><span class="sxs-lookup"><span data-stu-id="449a9-139">System.String</span></span>

## <span data-ttu-id="449a9-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="449a9-140">OUTPUTS</span></span>

### <span data-ttu-id="449a9-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="449a9-141">System.Boolean</span></span>

## <span data-ttu-id="449a9-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="449a9-142">NOTES</span></span>

## <span data-ttu-id="449a9-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="449a9-143">RELATED LINKS</span></span>

[<span data-ttu-id="449a9-144">Neu – AzSearchService</span><span class="sxs-lookup"><span data-stu-id="449a9-144">New-AzSearchService</span></span>](./New-AzSearchService.md)

[<span data-ttu-id="449a9-145">Get-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="449a9-145">Get-AzSearchService</span></span>](./Get-AzSearchService.md)

[<span data-ttu-id="449a9-146">Satz-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="449a9-146">Set-AzSearchService</span></span>](./Set-AzSearchService.md)


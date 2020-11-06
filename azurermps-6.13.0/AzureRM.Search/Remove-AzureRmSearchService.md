---
external help file: Microsoft.Azure.Commands.Management.Search.dll-Help.xml
Module Name: AzureRM.Search
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.search/remove-azurermsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Remove-AzureRmSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Remove-AzureRmSearchService.md
ms.openlocfilehash: c558a5d7228253e0a76b0d47fb21f581b4e06f11
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500118"
---
# <span data-ttu-id="eddc7-101">Remove-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="eddc7-101">Remove-AzureRmSearchService</span></span>

## <span data-ttu-id="eddc7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="eddc7-102">SYNOPSIS</span></span>
<span data-ttu-id="eddc7-103">Entfernen eines Azure-Suchdiensts</span><span class="sxs-lookup"><span data-stu-id="eddc7-103">Remove an Azure Search service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eddc7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="eddc7-104">SYNTAX</span></span>

### <span data-ttu-id="eddc7-105">ResourceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="eddc7-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzureRmSearchService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eddc7-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="eddc7-106">InputObjectParameterSet</span></span>
```
Remove-AzureRmSearchService [-InputObject] <PSSearchService> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eddc7-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="eddc7-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmSearchService [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eddc7-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="eddc7-108">DESCRIPTION</span></span>
<span data-ttu-id="eddc7-109">Das Cmdlet **Remove-AzureRmSearchService** entfernt einen Azure-Suchdienst mit dem angegebenen Parametern.</span><span class="sxs-lookup"><span data-stu-id="eddc7-109">The **Remove-AzureRmSearchService** cmdlet removes an Azure Search service with specified paramters.</span></span>

## <span data-ttu-id="eddc7-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="eddc7-110">EXAMPLES</span></span>

### <span data-ttu-id="eddc7-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="eddc7-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmSearchService -ResourceGroupName "TestAzureSearchPsGroup" -Name "pstestazuresearch01"

Confirm
Are you sure you want to remove Search Service 'pstestazuresearch01'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
PS C:\>
```

<span data-ttu-id="eddc7-112">Im Beispiel wird ein Azure-Suchdienst entfernt.</span><span class="sxs-lookup"><span data-stu-id="eddc7-112">The example removes an Azure Search service.</span></span>

## <span data-ttu-id="eddc7-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="eddc7-113">PARAMETERS</span></span>

### <span data-ttu-id="eddc7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eddc7-114">-DefaultProfile</span></span>
<span data-ttu-id="eddc7-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="eddc7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eddc7-116">-Force</span><span class="sxs-lookup"><span data-stu-id="eddc7-116">-Force</span></span>
<span data-ttu-id="eddc7-117">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="eddc7-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="eddc7-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="eddc7-118">-InputObject</span></span>
<span data-ttu-id="eddc7-119">Suchdienst Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="eddc7-119">Search Service Input Object.</span></span>

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

### <span data-ttu-id="eddc7-120">-Name</span><span class="sxs-lookup"><span data-stu-id="eddc7-120">-Name</span></span>
<span data-ttu-id="eddc7-121">Name des Suchdiensts</span><span class="sxs-lookup"><span data-stu-id="eddc7-121">Search Service name.</span></span>

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

### <span data-ttu-id="eddc7-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eddc7-122">-PassThru</span></span>
<span data-ttu-id="eddc7-123">Dieses Cmdlet gibt standardmäßig kein Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="eddc7-123">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="eddc7-124">Wenn dieser Schalter angegeben wird, wird true zurückgegeben, wenn er erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="eddc7-124">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="eddc7-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eddc7-125">-ResourceGroupName</span></span>
<span data-ttu-id="eddc7-126">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="eddc7-126">Resource Group name.</span></span>

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

### <span data-ttu-id="eddc7-127">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="eddc7-127">-ResourceId</span></span>
<span data-ttu-id="eddc7-128">Ressourcen-ID des Suchdiensts.</span><span class="sxs-lookup"><span data-stu-id="eddc7-128">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="eddc7-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="eddc7-129">-Confirm</span></span>
<span data-ttu-id="eddc7-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="eddc7-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eddc7-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eddc7-131">-WhatIf</span></span>
<span data-ttu-id="eddc7-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="eddc7-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eddc7-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="eddc7-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eddc7-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eddc7-134">CommonParameters</span></span>
<span data-ttu-id="eddc7-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eddc7-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eddc7-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eddc7-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eddc7-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="eddc7-137">INPUTS</span></span>

### <span data-ttu-id="eddc7-138">Microsoft. Azure. Commands. Management. search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="eddc7-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>
<span data-ttu-id="eddc7-139">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="eddc7-139">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="eddc7-140">System. String</span><span class="sxs-lookup"><span data-stu-id="eddc7-140">System.String</span></span>

## <span data-ttu-id="eddc7-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="eddc7-141">OUTPUTS</span></span>

### <span data-ttu-id="eddc7-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="eddc7-142">System.Boolean</span></span>

## <span data-ttu-id="eddc7-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="eddc7-143">NOTES</span></span>

## <span data-ttu-id="eddc7-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="eddc7-144">RELATED LINKS</span></span>

[<span data-ttu-id="eddc7-145">Neu – AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="eddc7-145">New-AzureRmSearchService</span></span>](./New-AzureRmSearchService.md)

[<span data-ttu-id="eddc7-146">Get-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="eddc7-146">Get-AzureRmSearchService</span></span>](./Get-AzureRmSearchService.md)

[<span data-ttu-id="eddc7-147">Satz-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="eddc7-147">Set-AzureRmSearchService</span></span>](./Set-AzureRmSearchService.md)


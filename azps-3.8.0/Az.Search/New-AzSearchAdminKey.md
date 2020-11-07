---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/new-azsearchadminkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchAdminKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchAdminKey.md
ms.openlocfilehash: ae925d39dab3b56e70cb7c42b320e57eb7f7811a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846779"
---
# <span data-ttu-id="21540-101">New-AzSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="21540-101">New-AzSearchAdminKey</span></span>

## <span data-ttu-id="21540-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="21540-102">SYNOPSIS</span></span>
<span data-ttu-id="21540-103">Regeneriert einen Administratorschlüssel des Azure-Suchdiensts.</span><span class="sxs-lookup"><span data-stu-id="21540-103">Regenerates an admin key of the Azure Search service.</span></span>

## <span data-ttu-id="21540-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="21540-104">SYNTAX</span></span>

### <span data-ttu-id="21540-105">ResourceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="21540-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzSearchAdminKey [-ResourceGroupName] <String> [-ServiceName] <String> -KeyKind <PSSearchAdminKeyKind>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21540-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="21540-106">ParentObjectParameterSet</span></span>
```
New-AzSearchAdminKey [-ParentObject] <PSSearchService> -KeyKind <PSSearchAdminKeyKind> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21540-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="21540-107">ParentResourceIdParameterSet</span></span>
```
New-AzSearchAdminKey [-ParentResourceId] <String> -KeyKind <PSSearchAdminKeyKind> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21540-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="21540-108">DESCRIPTION</span></span>
<span data-ttu-id="21540-109">Das Cmdlet **New-AzSearchAdminKey** generiert einen Administratorschlüssel des Azure-Suchdiensts erneut.</span><span class="sxs-lookup"><span data-stu-id="21540-109">The **New-AzSearchAdminKey** cmdlet regenerates an admin key of the Azure Search service.</span></span>

## <span data-ttu-id="21540-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="21540-110">EXAMPLES</span></span>

### <span data-ttu-id="21540-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="21540-111">Example 1</span></span>
```powershell
PS C:\> New-AzSearchAdminKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01" -KeyKind Primary

Confirm
Are you sure you want to regenerate 'Primary' key for Search Service 'pstestazuresearch01'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y

Primary                          Secondary
-------                          ---------
85B3813D11904B591BE8A196C2C743A1 CEF791D5BAC2E6C0B232C56702F21E87
```

<span data-ttu-id="21540-112">Im Beispiel wird der Primärschlüssel des Azure Search-Diensts erneut generiert.</span><span class="sxs-lookup"><span data-stu-id="21540-112">The example regenerates Primary key of the Azure Search Service.</span></span>

## <span data-ttu-id="21540-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="21540-113">PARAMETERS</span></span>

### <span data-ttu-id="21540-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21540-114">-DefaultProfile</span></span>
<span data-ttu-id="21540-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="21540-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21540-116">-Force</span><span class="sxs-lookup"><span data-stu-id="21540-116">-Force</span></span>
<span data-ttu-id="21540-117">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="21540-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="21540-118">-Keykind</span><span class="sxs-lookup"><span data-stu-id="21540-118">-KeyKind</span></span>
<span data-ttu-id="21540-119">Suchdienstadministrator-Schlüsseltyp (Primär/Sekundär).</span><span class="sxs-lookup"><span data-stu-id="21540-119">Search Service admin key kind (Primary/Secondary).</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchAdminKeyKind
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21540-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="21540-120">-ParentObject</span></span>
<span data-ttu-id="21540-121">Suchdienst Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="21540-121">Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: ParentObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="21540-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="21540-122">-ParentResourceId</span></span>
<span data-ttu-id="21540-123">Ressourcen-ID des Suchdiensts.</span><span class="sxs-lookup"><span data-stu-id="21540-123">Search Service Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ParentResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21540-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21540-124">-ResourceGroupName</span></span>
<span data-ttu-id="21540-125">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="21540-125">Resource Group name.</span></span>

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

### <span data-ttu-id="21540-126">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="21540-126">-ServiceName</span></span>
<span data-ttu-id="21540-127">Name des Suchdiensts</span><span class="sxs-lookup"><span data-stu-id="21540-127">Search Service name.</span></span>

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

### <span data-ttu-id="21540-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="21540-128">-Confirm</span></span>
<span data-ttu-id="21540-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="21540-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21540-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21540-130">-WhatIf</span></span>
<span data-ttu-id="21540-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="21540-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21540-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="21540-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21540-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21540-133">CommonParameters</span></span>
<span data-ttu-id="21540-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21540-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21540-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21540-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21540-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="21540-136">INPUTS</span></span>

### <span data-ttu-id="21540-137">Microsoft. Azure. Commands. Management. search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="21540-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="21540-138">System. String</span><span class="sxs-lookup"><span data-stu-id="21540-138">System.String</span></span>

## <span data-ttu-id="21540-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="21540-139">OUTPUTS</span></span>

### <span data-ttu-id="21540-140">Microsoft. Azure. Commands. Management. search. Models. PSSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="21540-140">Microsoft.Azure.Commands.Management.Search.Models.PSSearchAdminKey</span></span>

## <span data-ttu-id="21540-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="21540-141">NOTES</span></span>

## <span data-ttu-id="21540-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="21540-142">RELATED LINKS</span></span>

[<span data-ttu-id="21540-143">Get-AzSearchAdminKeyPair</span><span class="sxs-lookup"><span data-stu-id="21540-143">Get-AzSearchAdminKeyPair</span></span>](./Get-AzSearchAdminKeyPair.md)

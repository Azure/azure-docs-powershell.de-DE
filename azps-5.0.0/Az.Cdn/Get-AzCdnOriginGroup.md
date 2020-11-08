---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnorigingroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOriginGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOriginGroup.md
ms.openlocfilehash: 98c41f8e9e1592cf0405f42701fc19f3badd9553
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179740"
---
# <span data-ttu-id="59391-101">Get-AzCdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="59391-101">Get-AzCdnOriginGroup</span></span>

## <span data-ttu-id="59391-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="59391-102">SYNOPSIS</span></span>
<span data-ttu-id="59391-103">Ruft eine CDN-Ursprungsgruppe ab.</span><span class="sxs-lookup"><span data-stu-id="59391-103">Gets a CDN origin group</span></span>

## <span data-ttu-id="59391-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="59391-104">SYNTAX</span></span>

### <span data-ttu-id="59391-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="59391-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnOriginGroup -EndpointName <String> -OriginGroupName <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="59391-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="59391-106">ByResourceIdParameterSet</span></span>
```
Get-AzCdnOriginGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59391-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="59391-107">DESCRIPTION</span></span>
<span data-ttu-id="59391-108">Das Get-AzCdnOriginGroup-Cmdlet ruft eine CDN-Ursprungsgruppe ab.</span><span class="sxs-lookup"><span data-stu-id="59391-108">The Get-AzCdnOriginGroup cmdlet retrieves a CDN origin group.</span></span>

## <span data-ttu-id="59391-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="59391-109">EXAMPLES</span></span>

### <span data-ttu-id="59391-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="59391-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCdnOriginGroup -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginGroupName $originGroupName
```

<span data-ttu-id="59391-111">Mit diesem Befehl wird die Ursprungsgruppe innerhalb des angegebenen Endpunkts abgerufen.</span><span class="sxs-lookup"><span data-stu-id="59391-111">This command will get the origin group within the specified endpoint.</span></span>

## <span data-ttu-id="59391-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="59391-112">PARAMETERS</span></span>

### <span data-ttu-id="59391-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59391-113">-DefaultProfile</span></span>
<span data-ttu-id="59391-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="59391-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59391-115">-Endpunktname</span><span class="sxs-lookup"><span data-stu-id="59391-115">-EndpointName</span></span>
<span data-ttu-id="59391-116">Azure CDN-Endpunktname.</span><span class="sxs-lookup"><span data-stu-id="59391-116">Azure CDN endpoint name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59391-117">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="59391-117">-OriginGroupName</span></span>
<span data-ttu-id="59391-118">Name der Azure CDN-Ursprungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="59391-118">Azure CDN origin group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59391-119">-Profilname</span><span class="sxs-lookup"><span data-stu-id="59391-119">-ProfileName</span></span>
<span data-ttu-id="59391-120">Azure CDN-Profilname</span><span class="sxs-lookup"><span data-stu-id="59391-120">Azure CDN profile name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59391-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59391-121">-ResourceGroupName</span></span>
<span data-ttu-id="59391-122">Die Ressourcengruppe des Azure CDN-Profils.</span><span class="sxs-lookup"><span data-stu-id="59391-122">The resource group of the Azure CDN profile.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59391-123">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="59391-123">-ResourceId</span></span>
<span data-ttu-id="59391-124">Ressourcen-ID für die Gruppe "Ursprung"</span><span class="sxs-lookup"><span data-stu-id="59391-124">Resource Id for the the origin group</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59391-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59391-125">CommonParameters</span></span>
<span data-ttu-id="59391-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59391-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59391-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="59391-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59391-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="59391-128">INPUTS</span></span>

### <span data-ttu-id="59391-129">Keine</span><span class="sxs-lookup"><span data-stu-id="59391-129">None</span></span>

## <span data-ttu-id="59391-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="59391-130">OUTPUTS</span></span>

### <span data-ttu-id="59391-131">System. Object</span><span class="sxs-lookup"><span data-stu-id="59391-131">System.Object</span></span>

## <span data-ttu-id="59391-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="59391-132">NOTES</span></span>

## <span data-ttu-id="59391-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="59391-133">RELATED LINKS</span></span>

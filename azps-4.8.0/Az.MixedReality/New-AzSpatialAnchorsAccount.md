---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/new-azspatialanchorsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzSpatialAnchorsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzSpatialAnchorsAccount.md
ms.openlocfilehash: 0b61764d358cc234f66dc8bb24249ca93a4e9919
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173701"
---
# <span data-ttu-id="c19df-101">New-AzSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="c19df-101">New-AzSpatialAnchorsAccount</span></span>

## <span data-ttu-id="c19df-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c19df-102">SYNOPSIS</span></span>
<span data-ttu-id="c19df-103">Erstellen eines Spatial-Anker Kontos</span><span class="sxs-lookup"><span data-stu-id="c19df-103">Create Spatial Anchors Account</span></span>

## <span data-ttu-id="c19df-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c19df-104">SYNTAX</span></span>

```
New-AzSpatialAnchorsAccount -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c19df-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c19df-105">DESCRIPTION</span></span>
<span data-ttu-id="c19df-106">Erstellen Sie ein neues räumliches Anker Konto in bestimmten Abonnements, Ressourcengruppen und Regionen.</span><span class="sxs-lookup"><span data-stu-id="c19df-106">Create a new Spatial Anchors Account in certain Subscription, Resource Group and Region.</span></span>

## <span data-ttu-id="c19df-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c19df-107">EXAMPLES</span></span>

### <span data-ttu-id="c19df-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c19df-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmSpatialAnchorsAccount -ResourceGroup rg1 -Name example -Location centralus

ResourceGroupName   : rg1
AccountId           : 5f70bc31-a5da-4dd7-b5ec-ccdf806ff0ef
AccountEndpoint     : https://mrc-anchor-prod.trafficmanager.net/Accounts/5f70bc31-a5da-4dd7-b5ec-ccdf806ff0ef/
AccountDomain       : mixedreality.azure.com
Tags                : {}
Location            : centralus
Id                  : /subscriptions/10438cf7-a794-4c7b-ad4c-5ddc1313ba7d/resourceGroups/rg1/providers/Microsoft.MixedReality/SpatialAnchorsAccounts/example
Name                : example
Type                : Microsoft.MixedReality/SpatialAnchorsAccounts
```

<span data-ttu-id="c19df-109">Erstellen Sie ein neues Raum Anker Konto "Beispiel" im aktuellen Abonnement, Ressourcengruppe "RG1" und zentral USA.</span><span class="sxs-lookup"><span data-stu-id="c19df-109">Create a new Spatial Anchors Account "example" in current Subscription, Resource Group "rg1" and Central US.</span></span>

## <span data-ttu-id="c19df-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="c19df-110">PARAMETERS</span></span>

### <span data-ttu-id="c19df-111">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c19df-111">-Confirm</span></span>
<span data-ttu-id="c19df-112">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c19df-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c19df-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c19df-113">-DefaultProfile</span></span>
<span data-ttu-id="c19df-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c19df-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c19df-115">-Standort</span><span class="sxs-lookup"><span data-stu-id="c19df-115">-Location</span></span>
<span data-ttu-id="c19df-116">Standort des Standorts des räumlichen Ankers</span><span class="sxs-lookup"><span data-stu-id="c19df-116">Spatial Anchors Account Location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c19df-117">-Name</span><span class="sxs-lookup"><span data-stu-id="c19df-117">-Name</span></span>
<span data-ttu-id="c19df-118">Konto Name für Spatial-Anker</span><span class="sxs-lookup"><span data-stu-id="c19df-118">Spatial Anchors Account Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SpatialAnchorsAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c19df-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c19df-119">-ResourceGroupName</span></span>
<span data-ttu-id="c19df-120">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c19df-120">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c19df-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c19df-121">-WhatIf</span></span>
<span data-ttu-id="c19df-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c19df-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c19df-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c19df-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c19df-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c19df-124">CommonParameters</span></span>
<span data-ttu-id="c19df-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c19df-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="c19df-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c19df-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c19df-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c19df-127">INPUTS</span></span>

### <span data-ttu-id="c19df-128">Keine</span><span class="sxs-lookup"><span data-stu-id="c19df-128">None</span></span>

## <span data-ttu-id="c19df-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c19df-129">OUTPUTS</span></span>

### <span data-ttu-id="c19df-130">Microsoft. Azure. Commands. MixedReality. SpatialAnchorsAccount. PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="c19df-130">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

## <span data-ttu-id="c19df-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="c19df-131">NOTES</span></span>

## <span data-ttu-id="c19df-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c19df-132">RELATED LINKS</span></span>

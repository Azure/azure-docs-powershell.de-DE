---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/new-azspatialanchorsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzSpatialAnchorsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzSpatialAnchorsAccount.md
ms.openlocfilehash: 7ead8ca49491db9443f6cb0b06f87cb4917fc375
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93819032"
---
# <span data-ttu-id="073a0-101">New-AzSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="073a0-101">New-AzSpatialAnchorsAccount</span></span>

## <span data-ttu-id="073a0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="073a0-102">SYNOPSIS</span></span>
<span data-ttu-id="073a0-103">Erstellen eines Spatial-Anker Kontos</span><span class="sxs-lookup"><span data-stu-id="073a0-103">Create Spatial Anchors Account</span></span>

## <span data-ttu-id="073a0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="073a0-104">SYNTAX</span></span>

```
New-AzSpatialAnchorsAccount -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="073a0-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="073a0-105">DESCRIPTION</span></span>
<span data-ttu-id="073a0-106">Erstellen Sie ein neues räumliches Inelligence-Konto in bestimmten Abonnements, Ressourcengruppen und Regionen.</span><span class="sxs-lookup"><span data-stu-id="073a0-106">Create a new Spatial Inelligence Account in certain Subscription, Resource Group and Region.</span></span>

## <span data-ttu-id="073a0-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="073a0-107">EXAMPLES</span></span>

### <span data-ttu-id="073a0-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="073a0-108">Example 1</span></span>
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

<span data-ttu-id="073a0-109">Erstellen Sie ein neues Raum Anker Konto "Beispiel" im aktuellen Abonnement, Ressourcengruppe "RG1" und zentral USA.</span><span class="sxs-lookup"><span data-stu-id="073a0-109">Create a new Spatial Anchors Account "example" in current Subscription, Resource Group "rg1" and Central US.</span></span>

## <span data-ttu-id="073a0-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="073a0-110">PARAMETERS</span></span>

### <span data-ttu-id="073a0-111">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="073a0-111">-Confirm</span></span>
<span data-ttu-id="073a0-112">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="073a0-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="073a0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="073a0-113">-DefaultProfile</span></span>
<span data-ttu-id="073a0-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="073a0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="073a0-115">-Standort</span><span class="sxs-lookup"><span data-stu-id="073a0-115">-Location</span></span>
<span data-ttu-id="073a0-116">Standort des Standorts des räumlichen Ankers</span><span class="sxs-lookup"><span data-stu-id="073a0-116">Spatial Anchors Account Location.</span></span>

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

### <span data-ttu-id="073a0-117">-Name</span><span class="sxs-lookup"><span data-stu-id="073a0-117">-Name</span></span>
<span data-ttu-id="073a0-118">Konto Name für Spatial-Anker</span><span class="sxs-lookup"><span data-stu-id="073a0-118">Spatial Anchors Account Name.</span></span>

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

### <span data-ttu-id="073a0-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="073a0-119">-ResourceGroupName</span></span>
<span data-ttu-id="073a0-120">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="073a0-120">Resource Group Name.</span></span>

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

### <span data-ttu-id="073a0-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="073a0-121">-WhatIf</span></span>
<span data-ttu-id="073a0-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="073a0-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="073a0-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="073a0-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="073a0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="073a0-124">CommonParameters</span></span>
<span data-ttu-id="073a0-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="073a0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="073a0-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="073a0-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="073a0-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="073a0-127">INPUTS</span></span>

### <span data-ttu-id="073a0-128">Keine</span><span class="sxs-lookup"><span data-stu-id="073a0-128">None</span></span>

## <span data-ttu-id="073a0-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="073a0-129">OUTPUTS</span></span>

### <span data-ttu-id="073a0-130">Microsoft. Azure. Commands. MixedReality. SpatialAnchorsAccount. PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="073a0-130">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

## <span data-ttu-id="073a0-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="073a0-131">NOTES</span></span>

## <span data-ttu-id="073a0-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="073a0-132">RELATED LINKS</span></span>

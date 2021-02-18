---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 02396628-5E3E-49A6-8377-3F6DC488FEF8
online version: ''
schema: 2.0.0
ms.openlocfilehash: ee948161f101b83a4892441286b760a044e64358
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100405821"
---
# <span data-ttu-id="b30aa-101">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="b30aa-101">Get-AzureSiteRecoveryProtectionContainer</span></span>

## <span data-ttu-id="b30aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b30aa-102">SYNOPSIS</span></span>
<span data-ttu-id="b30aa-103">Ruft Schutzcontainer für einen Websitewiederherstellungstresor ab.</span><span class="sxs-lookup"><span data-stu-id="b30aa-103">Gets protection containers for a Site Recovery vault.</span></span>

## <span data-ttu-id="b30aa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b30aa-104">SYNTAX</span></span>

### <span data-ttu-id="b30aa-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="b30aa-105">Default (Default)</span></span>
```
Get-AzureSiteRecoveryProtectionContainer [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="b30aa-106">ById</span><span class="sxs-lookup"><span data-stu-id="b30aa-106">ById</span></span>
```
Get-AzureSiteRecoveryProtectionContainer -Id <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="b30aa-107">ByName</span><span class="sxs-lookup"><span data-stu-id="b30aa-107">ByName</span></span>
```
Get-AzureSiteRecoveryProtectionContainer -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b30aa-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b30aa-108">DESCRIPTION</span></span>
<span data-ttu-id="b30aa-109">Das **Cmdlet "Get-AzureSiteRecoveryProtectionContainer"** ruft Schutzcontainer für den aktuellen Azure Site Recovery Vault ab.</span><span class="sxs-lookup"><span data-stu-id="b30aa-109">The **Get-AzureSiteRecoveryProtectionContainer** cmdlet gets protection containers for the current Azure Site Recovery vault.</span></span>
<span data-ttu-id="b30aa-110">Ein Schutzcontainer ist ein logischer Container für geschützte Objekte wie virtuelle Computer.</span><span class="sxs-lookup"><span data-stu-id="b30aa-110">A protection container is a logical container for protected objects such as virtual machines.</span></span>
<span data-ttu-id="b30aa-111">Schutzrichtlinien definieren Replikationseinstellungen für geschützte Elemente und können einem Schutzcontainer zugeordnet und auf eine geschützte Entität angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="b30aa-111">Protection policies define replication settings for protected items and can be associated with a protection container and applied to a protected entity.</span></span>

## <span data-ttu-id="b30aa-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b30aa-112">EXAMPLES</span></span>

### <span data-ttu-id="b30aa-113">Beispiel 1: Geschützte Container erhalten</span><span class="sxs-lookup"><span data-stu-id="b30aa-113">Example 1: Get protected containers</span></span>
```
PS C:\> Get-AzureSiteRecoveryProtectionContainer
Name                        : PrimaryCloud
ID                          : fd00d920-79e4-4f2d-a282-a779c0cecb7f_ce995917-c962-45d0-b7f3-9f408a4e1429
FabricObjectId              : fd00d920-79e4-4f2d-a282-a779c0cecb7f
FabricType                  : VMM
Type                        : VMM
ServerId                    : fd00d920-79e4-4f2d-a282-a779c0cecb7f
Role                        : Primary
AvailableProtectionProfiles : {ab01dcbe-9da0-4c31-9564-d6904cfadfde, ad388147-83de-4d2f-a09d-fa46c626747e}
```

<span data-ttu-id="b30aa-114">Dieser Befehl ruft die geschützten Container für den aktuellen Tresor ab.</span><span class="sxs-lookup"><span data-stu-id="b30aa-114">This command gets the protected containers for the current vault.</span></span>

## <span data-ttu-id="b30aa-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b30aa-115">PARAMETERS</span></span>

### <span data-ttu-id="b30aa-116">-ID</span><span class="sxs-lookup"><span data-stu-id="b30aa-116">-Id</span></span>
<span data-ttu-id="b30aa-117">Gibt die ID eines geschützten Containers an, den Sie erhalten müssen.</span><span class="sxs-lookup"><span data-stu-id="b30aa-117">Specifies the ID of a protected container to get.</span></span>

```yaml
Type: String
Parameter Sets: ById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b30aa-118">-Name</span><span class="sxs-lookup"><span data-stu-id="b30aa-118">-Name</span></span>
<span data-ttu-id="b30aa-119">Gibt den Namen eines zu erhaltenden Schutzcontainers an.</span><span class="sxs-lookup"><span data-stu-id="b30aa-119">Specifies the name of a protection container to get.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b30aa-120">-Profile</span><span class="sxs-lookup"><span data-stu-id="b30aa-120">-Profile</span></span>
<span data-ttu-id="b30aa-121">Gibt das Azure-Profil an, aus dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="b30aa-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b30aa-122">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="b30aa-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b30aa-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b30aa-123">CommonParameters</span></span>
<span data-ttu-id="b30aa-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b30aa-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b30aa-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b30aa-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b30aa-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b30aa-126">INPUTS</span></span>

## <span data-ttu-id="b30aa-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b30aa-127">OUTPUTS</span></span>

## <span data-ttu-id="b30aa-128">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b30aa-128">NOTES</span></span>

## <span data-ttu-id="b30aa-129">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b30aa-129">RELATED LINKS</span></span>





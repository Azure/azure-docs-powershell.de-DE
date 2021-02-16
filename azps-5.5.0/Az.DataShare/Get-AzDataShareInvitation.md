---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatashareinvitation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareInvitation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareInvitation.md
ms.openlocfilehash: 0a723400bf92569a077abc64467c3cace56da0a6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100170813"
---
# <span data-ttu-id="dbcfb-101">Get-AzDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="dbcfb-101">Get-AzDataShareInvitation</span></span>

## <span data-ttu-id="dbcfb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dbcfb-102">SYNOPSIS</span></span>
<span data-ttu-id="dbcfb-103">Ruft die Informationseinladung zur Datenfreigabe ab.</span><span class="sxs-lookup"><span data-stu-id="dbcfb-103">Gets information invitation of data share.</span></span>

## <span data-ttu-id="dbcfb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dbcfb-104">SYNTAX</span></span>

### <span data-ttu-id="dbcfb-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="dbcfb-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareInvitation -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dbcfb-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dbcfb-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareInvitation -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dbcfb-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dbcfb-107">DESCRIPTION</span></span>
<span data-ttu-id="dbcfb-108">Das **Cmdlet "Get-AzDataShareInvitation"** ruft Informationen zu Einladungen ab, die in der Datenfreigabe hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="dbcfb-108">The **Get-AzDataShareInvitation** cmdlet gets information on invitations added in data share.</span></span> <span data-ttu-id="dbcfb-109">Wenn Sie den Namen der Einladung angeben, ruft dieses Cmdlet Informationen zur Einladung ab.</span><span class="sxs-lookup"><span data-stu-id="dbcfb-109">If you specify the name of the invitation, this cmdlet gets information about the invitation.</span></span> <span data-ttu-id="dbcfb-110">Wenn Sie keinen Namen angeben, ruft dieses Cmdlet Informationen zu allen Einladungen in einer Freigabe ab.</span><span class="sxs-lookup"><span data-stu-id="dbcfb-110">If you do not specify a name, this cmdlet gets information about all the invitations in a share.</span></span>

## <span data-ttu-id="dbcfb-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="dbcfb-111">EXAMPLES</span></span>

### <span data-ttu-id="dbcfb-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="dbcfb-112">Example 1</span></span>
```
PS C:\> Get-AzDataShareInvitation -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "AdsInvitation"

InvitationId     : 167e06ff-567f-4bc7-be0c-645a6de710f3
InvitationStatus : Pending
Sender           : adsprovider@microsoft.com
SentAt           : 7/8/2019 10:47:10 PM
TargetEmail      : adstest@microsoft.com
TargetObjectId   :
TargetTenantId   :
Id               : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shares/AdsShare/invitations/AdsInvitation
Name             : AdsInvitation
Type             : Microsoft.DataShare/Invitations
```

<span data-ttu-id="dbcfb-113">Diese Befehle enthalten Informationen über Einladungen zu AdsInvitation, die in der Datenfreigabe von AdsShare vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="dbcfb-113">This commands provides information about invitation AdsInvitation present in data share AdsShare.</span></span>

## <span data-ttu-id="dbcfb-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dbcfb-114">PARAMETERS</span></span>

### <span data-ttu-id="dbcfb-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="dbcfb-115">-AccountName</span></span>
<span data-ttu-id="dbcfb-116">Name des Azure-Datenfreigabekontos</span><span class="sxs-lookup"><span data-stu-id="dbcfb-116">Azure data share account name</span></span>

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

### <span data-ttu-id="dbcfb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbcfb-117">-DefaultProfile</span></span>
<span data-ttu-id="dbcfb-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dbcfb-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dbcfb-119">-Name</span><span class="sxs-lookup"><span data-stu-id="dbcfb-119">-Name</span></span>
<span data-ttu-id="dbcfb-120">Name der Einladung zur Freigabe von Azure-Daten</span><span class="sxs-lookup"><span data-stu-id="dbcfb-120">Azure data share invitation name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbcfb-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbcfb-121">-ResourceGroupName</span></span>
<span data-ttu-id="dbcfb-122">Der Ressourcengruppenname des Azure Data Share-Kontos</span><span class="sxs-lookup"><span data-stu-id="dbcfb-122">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="dbcfb-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dbcfb-123">-ResourceId</span></span>
<span data-ttu-id="dbcfb-124">Die Ressourcen-ID der Azure-Datenfreigabeeinladung</span><span class="sxs-lookup"><span data-stu-id="dbcfb-124">The resource id of the azure data share invitation</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbcfb-125">-ShareName</span><span class="sxs-lookup"><span data-stu-id="dbcfb-125">-ShareName</span></span>
<span data-ttu-id="dbcfb-126">Name der Azure-Datenfreigabe</span><span class="sxs-lookup"><span data-stu-id="dbcfb-126">Azure data share name</span></span>

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

### <span data-ttu-id="dbcfb-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbcfb-127">CommonParameters</span></span>
<span data-ttu-id="dbcfb-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbcfb-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbcfb-129">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dbcfb-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbcfb-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="dbcfb-130">INPUTS</span></span>

### <span data-ttu-id="dbcfb-131">System.String</span><span class="sxs-lookup"><span data-stu-id="dbcfb-131">System.String</span></span>

## <span data-ttu-id="dbcfb-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="dbcfb-132">OUTPUTS</span></span>

### <span data-ttu-id="dbcfb-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="dbcfb-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="dbcfb-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="dbcfb-134">NOTES</span></span>

## <span data-ttu-id="dbcfb-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="dbcfb-135">RELATED LINKS</span></span>

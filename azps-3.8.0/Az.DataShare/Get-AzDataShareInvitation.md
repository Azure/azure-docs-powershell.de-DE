---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatashareinvitation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareInvitation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareInvitation.md
ms.openlocfilehash: e4bff18d5b77296b470dfab8f086c101afe8e423
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995664"
---
# <span data-ttu-id="fc35c-101">Get-AzDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="fc35c-101">Get-AzDataShareInvitation</span></span>

## <span data-ttu-id="fc35c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fc35c-102">SYNOPSIS</span></span>
<span data-ttu-id="fc35c-103">Ruft Informations Einladung zur Datenfreigabe ab.</span><span class="sxs-lookup"><span data-stu-id="fc35c-103">Gets information invitation of data share.</span></span>

## <span data-ttu-id="fc35c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fc35c-104">SYNTAX</span></span>

### <span data-ttu-id="fc35c-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="fc35c-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareInvitation -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fc35c-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc35c-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareInvitation -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fc35c-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fc35c-107">DESCRIPTION</span></span>
<span data-ttu-id="fc35c-108">Das Cmdlet " **Get-AzDataShareInvitation** " Ruft Informationen zu Einladungen auf, die in der Datenfreigabe hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="fc35c-108">The **Get-AzDataShareInvitation** cmdlet gets information on invitations added in data share.</span></span> <span data-ttu-id="fc35c-109">Wenn Sie den Namen der Einladung angeben, ruft dieses Cmdlet Informationen zur Einladung ab.</span><span class="sxs-lookup"><span data-stu-id="fc35c-109">If you specify the name of the invitation, this cmdlet gets information about the invitation.</span></span> <span data-ttu-id="fc35c-110">Wenn Sie keinen Namen angeben, ruft dieses Cmdlet Informationen zu allen Einladungen in einer Freigabe ab.</span><span class="sxs-lookup"><span data-stu-id="fc35c-110">If you do not specify a name, this cmdlet gets information about all the invitations in a share.</span></span>

## <span data-ttu-id="fc35c-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fc35c-111">EXAMPLES</span></span>

### <span data-ttu-id="fc35c-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fc35c-112">Example 1</span></span>
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

<span data-ttu-id="fc35c-113">Dieser Befehl enthält Informationen zu Einladungs-AdsInvitation, die in Datenfreigabe-AdsShare vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="fc35c-113">This commands provides information about invitation AdsInvitation present in data share AdsShare.</span></span>

## <span data-ttu-id="fc35c-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="fc35c-114">PARAMETERS</span></span>

### <span data-ttu-id="fc35c-115">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="fc35c-115">-AccountName</span></span>
<span data-ttu-id="fc35c-116">Name des Azure-Datenfreigabe Kontos</span><span class="sxs-lookup"><span data-stu-id="fc35c-116">Azure data share account name</span></span>

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

### <span data-ttu-id="fc35c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc35c-117">-DefaultProfile</span></span>
<span data-ttu-id="fc35c-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fc35c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc35c-119">-Name</span><span class="sxs-lookup"><span data-stu-id="fc35c-119">-Name</span></span>
<span data-ttu-id="fc35c-120">Name der Einladung zu Azure Data Freigabe</span><span class="sxs-lookup"><span data-stu-id="fc35c-120">Azure data share invitation name</span></span>

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

### <span data-ttu-id="fc35c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc35c-121">-ResourceGroupName</span></span>
<span data-ttu-id="fc35c-122">Der Name der Ressourcengruppe des Azure Data Share-Kontos</span><span class="sxs-lookup"><span data-stu-id="fc35c-122">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="fc35c-123">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="fc35c-123">-ResourceId</span></span>
<span data-ttu-id="fc35c-124">Die Ressourcen-ID der Azure Data Share-Einladung</span><span class="sxs-lookup"><span data-stu-id="fc35c-124">The resource id of the azure data share invitation</span></span>

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

### <span data-ttu-id="fc35c-125">-Freigabename</span><span class="sxs-lookup"><span data-stu-id="fc35c-125">-ShareName</span></span>
<span data-ttu-id="fc35c-126">Name der Azure-Datenfreigabe</span><span class="sxs-lookup"><span data-stu-id="fc35c-126">Azure data share name</span></span>

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

### <span data-ttu-id="fc35c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc35c-127">CommonParameters</span></span>
<span data-ttu-id="fc35c-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc35c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc35c-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc35c-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc35c-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fc35c-130">INPUTS</span></span>

### <span data-ttu-id="fc35c-131">System. String</span><span class="sxs-lookup"><span data-stu-id="fc35c-131">System.String</span></span>

## <span data-ttu-id="fc35c-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fc35c-132">OUTPUTS</span></span>

### <span data-ttu-id="fc35c-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="fc35c-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="fc35c-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="fc35c-134">NOTES</span></span>

## <span data-ttu-id="fc35c-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fc35c-135">RELATED LINKS</span></span>

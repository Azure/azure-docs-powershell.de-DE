---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 7C695E83-78AA-4008-91D6-D6B23BC96B92
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryRecoveryPlan.md
ms.openlocfilehash: 5657701475e81b302d761193cd542ee38ea9c16e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496833"
---
# <span data-ttu-id="5a025-101">Remove-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="5a025-101">Remove-AzureRmSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="5a025-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5a025-102">SYNOPSIS</span></span>
<span data-ttu-id="5a025-103">Entfernt einen Website Wiederherstellungsplan aus der Websitewiederherstellung.</span><span class="sxs-lookup"><span data-stu-id="5a025-103">Removes a site recovery plan from Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5a025-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5a025-104">SYNTAX</span></span>

### <span data-ttu-id="5a025-105">ByObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="5a025-105">ByObject (Default)</span></span>
```
Remove-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a025-106">ByName</span><span class="sxs-lookup"><span data-stu-id="5a025-106">ByName</span></span>
```
Remove-AzureRmSiteRecoveryRecoveryPlan -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5a025-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5a025-107">DESCRIPTION</span></span>
<span data-ttu-id="5a025-108">Das Cmdlet **Remove-AzureRmSiteRecoveryRecoveryPlan** entfernt einen Website Wiederherstellungsplan aus der aktuellen Azure Site-Wiederherstellung.</span><span class="sxs-lookup"><span data-stu-id="5a025-108">The **Remove-AzureRmSiteRecoveryRecoveryPlan** cmdlet removes a site recovery plan from the current Azure Site Recovery.</span></span>

## <span data-ttu-id="5a025-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5a025-109">EXAMPLES</span></span>

### <span data-ttu-id="5a025-110">Beispiel 1: Entfernen eines Wiederherstellungsplans</span><span class="sxs-lookup"><span data-stu-id="5a025-110">Example 1: Remove a recovery plan</span></span>
```
PS C:\>$RecoveryPlan = Get-AzureRmSiteRecoveryRecoveryPlan 
PS C:\> Remove-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan $RecoveryPlan
```

<span data-ttu-id="5a025-111">Der erste Befehl verwendet das Get-AzureRmSiteRecoveryRecoveryPlan-Cmdlet, um den Website Wiederherstellungsplan abzurufen, und speichert ihn dann in der $RecoveryPlan-Variablen.</span><span class="sxs-lookup"><span data-stu-id="5a025-111">The first command uses the Get-AzureRmSiteRecoveryRecoveryPlan cmdlet to get the Site Recovery plan, and then stores it in the $RecoveryPlan variable.</span></span>

<span data-ttu-id="5a025-112">Der zweite Befehl entfernt den Wiederherstellungsplan in $RecoveryPlan.</span><span class="sxs-lookup"><span data-stu-id="5a025-112">The second command removes the recovery plan in $RecoveryPlan.</span></span>

## <span data-ttu-id="5a025-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="5a025-113">PARAMETERS</span></span>

### <span data-ttu-id="5a025-114">-Name</span><span class="sxs-lookup"><span data-stu-id="5a025-114">-Name</span></span>
<span data-ttu-id="5a025-115">Gibt den Namen des Wiederherstellungsplans an, den dieses Cmdlet entfernt.</span><span class="sxs-lookup"><span data-stu-id="5a025-115">Specifies the name of the recovery plan that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a025-116">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="5a025-116">-RecoveryPlan</span></span>
<span data-ttu-id="5a025-117">Gibt den Wiederherstellungsplan an, den dieses Cmdlet entfernt.</span><span class="sxs-lookup"><span data-stu-id="5a025-117">Specifies the recovery plan that this cmdlet removes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5a025-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a025-118">-DefaultProfile</span></span>
<span data-ttu-id="5a025-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5a025-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5a025-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a025-120">CommonParameters</span></span>
<span data-ttu-id="5a025-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a025-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a025-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a025-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a025-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5a025-123">INPUTS</span></span>

### <span data-ttu-id="5a025-124">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="5a025-124">ASRRecoveryPlan</span></span>
<span data-ttu-id="5a025-125">Der Parameter "RecoveryPlan" akzeptiert den Wert vom Typ "ASRRecoveryPlan" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="5a025-125">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

## <span data-ttu-id="5a025-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5a025-126">OUTPUTS</span></span>

## <span data-ttu-id="5a025-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="5a025-127">NOTES</span></span>

## <span data-ttu-id="5a025-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5a025-128">RELATED LINKS</span></span>

[<span data-ttu-id="5a025-129">Get-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="5a025-129">Get-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Get-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="5a025-130">Neu – AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="5a025-130">New-AzureRmSiteRecoveryRecoveryPlan</span></span>](./New-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="5a025-131">Update-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="5a025-131">Update-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Update-AzureRmSiteRecoveryRecoveryPlan.md)



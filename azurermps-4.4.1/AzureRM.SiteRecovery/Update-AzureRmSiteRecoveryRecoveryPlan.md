---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: BA387784-DFF5-4801-93F3-386454040B53
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryRecoveryPlan.md
ms.openlocfilehash: d497938a8a68d3efc6cafd1640de8d0be738b113
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664973"
---
# <span data-ttu-id="b4d07-101">Update-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="b4d07-101">Update-AzureRmSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="b4d07-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b4d07-102">SYNOPSIS</span></span>
<span data-ttu-id="b4d07-103">Aktualisiert einen Wiederherstellungsplan in der Websitewiederherstellung.</span><span class="sxs-lookup"><span data-stu-id="b4d07-103">Updates a recovery plan in Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b4d07-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b4d07-104">SYNTAX</span></span>

### <span data-ttu-id="b4d07-105">ByRPObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="b4d07-105">ByRPObject (Default)</span></span>
```
Update-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b4d07-106">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="b4d07-106">ByRPFile</span></span>
```
Update-AzureRmSiteRecoveryRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b4d07-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b4d07-107">DESCRIPTION</span></span>
<span data-ttu-id="b4d07-108">Das Cmdlet **Update-AzureRmSiteRecoveryRecoveryPlan** aktualisiert einen Wiederherstellungsplan in Azure Site Recovery und veröffentlicht ihn dann.</span><span class="sxs-lookup"><span data-stu-id="b4d07-108">The **Update-AzureRmSiteRecoveryRecoveryPlan** cmdlet updates a recovery plan in Azure Site Recovery and then publishes it.</span></span>

## <span data-ttu-id="b4d07-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b4d07-109">EXAMPLES</span></span>

### <span data-ttu-id="b4d07-110">Beispiel 1: Aktualisieren eines Wiederherstellungsplans</span><span class="sxs-lookup"><span data-stu-id="b4d07-110">Example 1: Update a recovery plan</span></span>
```
PS C:\>Update-AzureRmSiteRecoveryRecoveryPlan -File "C:\Users\Contoso\Desktop\RecoveryPlan.xml"
```

<span data-ttu-id="b4d07-111">Dieser Befehl aktualisiert den angegebenen Wiederherstellungsplan und veröffentlicht ihn dann.</span><span class="sxs-lookup"><span data-stu-id="b4d07-111">This command updates the specified recovery plan, and then publishes it.</span></span>

## <span data-ttu-id="b4d07-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="b4d07-112">PARAMETERS</span></span>

### <span data-ttu-id="b4d07-113">-Path</span><span class="sxs-lookup"><span data-stu-id="b4d07-113">-Path</span></span>
<span data-ttu-id="b4d07-114">Gibt den Pfad der Wiederherstellungsplan Datei des Wiederherstellungsplans an, den dieses Cmdlet aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="b4d07-114">Specifies the path of the recovery plan file of the recovery plan that this cmdlet updates.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4d07-115">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="b4d07-115">-RecoveryPlan</span></span>
<span data-ttu-id="b4d07-116">Gibt einen Wiederherstellungsplan an, den dieses Cmdlet aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="b4d07-116">Specifies a recovery plan that this cmdlet updates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b4d07-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4d07-117">-DefaultProfile</span></span>
<span data-ttu-id="b4d07-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b4d07-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4d07-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4d07-119">CommonParameters</span></span>
<span data-ttu-id="b4d07-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4d07-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4d07-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4d07-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4d07-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b4d07-122">INPUTS</span></span>

### <span data-ttu-id="b4d07-123">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="b4d07-123">ASRRecoveryPlan</span></span>
<span data-ttu-id="b4d07-124">Der Parameter "RecoveryPlan" akzeptiert den Wert vom Typ "ASRRecoveryPlan" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="b4d07-124">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

## <span data-ttu-id="b4d07-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b4d07-125">OUTPUTS</span></span>

## <span data-ttu-id="b4d07-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="b4d07-126">NOTES</span></span>

## <span data-ttu-id="b4d07-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b4d07-127">RELATED LINKS</span></span>

[<span data-ttu-id="b4d07-128">Get-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="b4d07-128">Get-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Get-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="b4d07-129">Neu – AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="b4d07-129">New-AzureRmSiteRecoveryRecoveryPlan</span></span>](./New-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="b4d07-130">Remove-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="b4d07-130">Remove-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Remove-AzureRmSiteRecoveryRecoveryPlan.md)



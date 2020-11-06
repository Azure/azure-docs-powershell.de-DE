---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: BA387784-DFF5-4801-93F3-386454040B53
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/update-azurermsiterecoveryrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryRecoveryPlan.md
ms.openlocfilehash: 594cb9af7c1afb82187003e3ddd7c085a254c59e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476537"
---
# <span data-ttu-id="233f4-101">Update-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="233f4-101">Update-AzureRmSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="233f4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="233f4-102">SYNOPSIS</span></span>
<span data-ttu-id="233f4-103">Aktualisiert einen Wiederherstellungsplan in der Websitewiederherstellung.</span><span class="sxs-lookup"><span data-stu-id="233f4-103">Updates a recovery plan in Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="233f4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="233f4-104">SYNTAX</span></span>

### <span data-ttu-id="233f4-105">ByRPObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="233f4-105">ByRPObject (Default)</span></span>
```
Update-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="233f4-106">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="233f4-106">ByRPFile</span></span>
```
Update-AzureRmSiteRecoveryRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="233f4-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="233f4-107">DESCRIPTION</span></span>
<span data-ttu-id="233f4-108">Das Cmdlet **Update-AzureRmSiteRecoveryRecoveryPlan** aktualisiert einen Wiederherstellungsplan in Azure Site Recovery und veröffentlicht ihn dann.</span><span class="sxs-lookup"><span data-stu-id="233f4-108">The **Update-AzureRmSiteRecoveryRecoveryPlan** cmdlet updates a recovery plan in Azure Site Recovery and then publishes it.</span></span>

## <span data-ttu-id="233f4-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="233f4-109">EXAMPLES</span></span>

### <span data-ttu-id="233f4-110">Beispiel 1: Aktualisieren eines Wiederherstellungsplans</span><span class="sxs-lookup"><span data-stu-id="233f4-110">Example 1: Update a recovery plan</span></span>
```
PS C:\>Update-AzureRmSiteRecoveryRecoveryPlan -File "C:\Users\Contoso\Desktop\RecoveryPlan.xml"
```

<span data-ttu-id="233f4-111">Dieser Befehl aktualisiert den angegebenen Wiederherstellungsplan und veröffentlicht ihn dann.</span><span class="sxs-lookup"><span data-stu-id="233f4-111">This command updates the specified recovery plan, and then publishes it.</span></span>

## <span data-ttu-id="233f4-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="233f4-112">PARAMETERS</span></span>

### <span data-ttu-id="233f4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="233f4-113">-DefaultProfile</span></span>
<span data-ttu-id="233f4-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="233f4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="233f4-115">-Path</span><span class="sxs-lookup"><span data-stu-id="233f4-115">-Path</span></span>
<span data-ttu-id="233f4-116">Gibt den Pfad der Wiederherstellungsplan Datei des Wiederherstellungsplans an, den dieses Cmdlet aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="233f4-116">Specifies the path of the recovery plan file of the recovery plan that this cmdlet updates.</span></span>

```yaml
Type: String
Parameter Sets: ByRPFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="233f4-117">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="233f4-117">-RecoveryPlan</span></span>
<span data-ttu-id="233f4-118">Gibt einen Wiederherstellungsplan an, den dieses Cmdlet aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="233f4-118">Specifies a recovery plan that this cmdlet updates.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="233f4-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="233f4-119">CommonParameters</span></span>
<span data-ttu-id="233f4-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="233f4-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="233f4-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="233f4-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="233f4-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="233f4-122">INPUTS</span></span>

### <span data-ttu-id="233f4-123">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="233f4-123">ASRRecoveryPlan</span></span>
<span data-ttu-id="233f4-124">Der Parameter "RecoveryPlan" akzeptiert den Wert vom Typ "ASRRecoveryPlan" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="233f4-124">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

## <span data-ttu-id="233f4-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="233f4-125">OUTPUTS</span></span>

## <span data-ttu-id="233f4-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="233f4-126">NOTES</span></span>

## <span data-ttu-id="233f4-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="233f4-127">RELATED LINKS</span></span>

[<span data-ttu-id="233f4-128">Get-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="233f4-128">Get-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Get-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="233f4-129">Neu – AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="233f4-129">New-AzureRmSiteRecoveryRecoveryPlan</span></span>](./New-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="233f4-130">Remove-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="233f4-130">Remove-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Remove-AzureRmSiteRecoveryRecoveryPlan.md)



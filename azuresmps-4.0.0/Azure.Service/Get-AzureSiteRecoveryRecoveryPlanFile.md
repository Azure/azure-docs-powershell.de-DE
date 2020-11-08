---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 00B8AB6D-02E0-45B5-AB69-49FC69246A34
online version: ''
schema: 2.0.0
ms.openlocfilehash: fb66f34cea13ac95cac47738e7cec214a6a10103
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005789"
---
# <span data-ttu-id="619b6-101">Get-AzureSiteRecoveryRecoveryPlanFile</span><span class="sxs-lookup"><span data-stu-id="619b6-101">Get-AzureSiteRecoveryRecoveryPlanFile</span></span>

## <span data-ttu-id="619b6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="619b6-102">SYNOPSIS</span></span>
<span data-ttu-id="619b6-103">Downloadet einen Azure Site Recovery Plan im XML-Format.</span><span class="sxs-lookup"><span data-stu-id="619b6-103">Downloads an Azure Site Recovery plan in XML format.</span></span>

## <span data-ttu-id="619b6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="619b6-104">SYNTAX</span></span>

### <span data-ttu-id="619b6-105">ByRPObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="619b6-105">ByRPObject (Default)</span></span>
```
Get-AzureSiteRecoveryRecoveryPlanFile -Path <String> -RecoveryPlan <ASRRecoveryPlan>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="619b6-106">ById</span><span class="sxs-lookup"><span data-stu-id="619b6-106">ById</span></span>
```
Get-AzureSiteRecoveryRecoveryPlanFile -Path <String> -Id <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="619b6-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="619b6-107">DESCRIPTION</span></span>
<span data-ttu-id="619b6-108">Das Cmdlet " **Get-AzureSiteRecoveryRecoveryPlanFile** " downloadet einen Azure Site Recovery Plan im XML-Format.</span><span class="sxs-lookup"><span data-stu-id="619b6-108">The **Get-AzureSiteRecoveryRecoveryPlanFile** cmdlet downloads an Azure Site Recovery plan in XML format.</span></span>
<span data-ttu-id="619b6-109">Sie können diese Datei verwenden, um den Wiederherstellungsplan zu aktualisieren und dann auf den Website Wiederherstellungsserver hochzuladen.</span><span class="sxs-lookup"><span data-stu-id="619b6-109">You can use this file to update the recovery plan and then upload it to the Site Recovery server.</span></span>

<span data-ttu-id="619b6-110">Ein Wiederherstellungsplan sammelt virtuelle Computer in einer Gruppe, um Failover und Wiederherstellung zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="619b6-110">A recovery plan gathers virtual machines in a group for the purposes of failover and recovery.</span></span>

## <span data-ttu-id="619b6-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="619b6-111">EXAMPLES</span></span>

### <span data-ttu-id="619b6-112">Beispiel 1: Abrufen einer Wiederherstellungsplan Datei</span><span class="sxs-lookup"><span data-stu-id="619b6-112">Example 1: Get a recovery plan file</span></span>
```
PS C:\> $RecoveryPlan = Get-AzureSiteRecoveryRecoveryPlan 
PS C:\> Get-AzureSiteRecoveryRecoveryPlanFile -RecoveryPlan $RecoveryPlan -Path "C:\Users\Contoso\Desktop\RecoveryPlan.xml"
```

<span data-ttu-id="619b6-113">Dieser Befehl verwendet das Cmdlet " **Get-AzureSiteRecoveryRecoveryPlan** ", um den Wiederherstellungsplan abzurufen, und speichert ihn dann in der $RecoveryPlan-Variablen.</span><span class="sxs-lookup"><span data-stu-id="619b6-113">This command uses the **Get-AzureSiteRecoveryRecoveryPlan** cmdlet to get the recovery plan, and then stores it in the $RecoveryPlan variable.</span></span>

<span data-ttu-id="619b6-114">Der zweite Befehl verwendet das **GetAzureSiteRecoveryRecoveryPlanFile** -Cmdlet, um die XML-Datei für den Website Wiederherstellungsplan in $RecoveryPlan abzurufen.</span><span class="sxs-lookup"><span data-stu-id="619b6-114">The second command uses the **GetAzureSiteRecoveryRecoveryPlanFile** cmdlet to get the site recovery plan XML file in $RecoveryPlan.</span></span>
<span data-ttu-id="619b6-115">Der Befehl speichert die XML-Datei unter dem angegebenen Pfad.</span><span class="sxs-lookup"><span data-stu-id="619b6-115">The command stores the XML file at the specified path.</span></span>

## <span data-ttu-id="619b6-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="619b6-116">PARAMETERS</span></span>

### <span data-ttu-id="619b6-117">-ID</span><span class="sxs-lookup"><span data-stu-id="619b6-117">-Id</span></span>
<span data-ttu-id="619b6-118">Gibt die ID des abzurufenden Wiederherstellungsplans an.</span><span class="sxs-lookup"><span data-stu-id="619b6-118">Specifies the ID of the recovery plan to get.</span></span>

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

### <span data-ttu-id="619b6-119">-Path</span><span class="sxs-lookup"><span data-stu-id="619b6-119">-Path</span></span>
<span data-ttu-id="619b6-120">Gibt den vollständigen Pfad zum Speichern der XML-Wiederherstellungsplan-Datei an.</span><span class="sxs-lookup"><span data-stu-id="619b6-120">Specifies the full path to store the recovery plan XML file.</span></span>

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

### <span data-ttu-id="619b6-121">-Profil</span><span class="sxs-lookup"><span data-stu-id="619b6-121">-Profile</span></span>
<span data-ttu-id="619b6-122">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="619b6-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="619b6-123">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="619b6-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="619b6-124">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="619b6-124">-RecoveryPlan</span></span>
<span data-ttu-id="619b6-125">Gibt ein **ASRRecoveryPlan** -Objekt an, aus dem der Wiederherstellungsplan abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="619b6-125">Specifies an **ASRRecoveryPlan** object from which to get the recovery plan.</span></span>
<span data-ttu-id="619b6-126">Verwenden Sie das Cmdlet **Get-AzureSiteRecoveryRecoveryPlan** , um ein **ASRRecoveryPlan** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="619b6-126">To obtain an **ASRRecoveryPlan** object, use the **Get-AzureSiteRecoveryRecoveryPlan** cmdlet.</span></span>

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

### <span data-ttu-id="619b6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="619b6-127">CommonParameters</span></span>
<span data-ttu-id="619b6-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="619b6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="619b6-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="619b6-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="619b6-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="619b6-130">INPUTS</span></span>

## <span data-ttu-id="619b6-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="619b6-131">OUTPUTS</span></span>

## <span data-ttu-id="619b6-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="619b6-132">NOTES</span></span>

## <span data-ttu-id="619b6-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="619b6-133">RELATED LINKS</span></span>

[<span data-ttu-id="619b6-134">Get-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="619b6-134">Get-AzureSiteRecoveryRecoveryPlan</span></span>](./Get-AzureSiteRecoveryRecoveryPlan.md)



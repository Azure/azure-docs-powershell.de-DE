---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 2F749E4A-149F-44E0-8AEB-F2C416140906
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7d1162ed2c9126942cc6ae31cbe31fdc2ef130d8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006182"
---
# <span data-ttu-id="75715-101">New-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="75715-101">New-AzureSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="75715-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="75715-102">SYNOPSIS</span></span>
<span data-ttu-id="75715-103">Erstellt einen Website Wiederherstellungsplan in der Websitewiederherstellung.</span><span class="sxs-lookup"><span data-stu-id="75715-103">Creates a site recovery plan in Site Recovery.</span></span>

## <span data-ttu-id="75715-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="75715-104">SYNTAX</span></span>

```
New-AzureSiteRecoveryRecoveryPlan -File <String> [-WaitForCompletion] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="75715-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="75715-105">DESCRIPTION</span></span>
<span data-ttu-id="75715-106">Das Cmdlet **New-AzureSiteRecoveryRecoveryPlan** erstellt einen Wiederherstellungsplan in Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="75715-106">The **New-AzureSiteRecoveryRecoveryPlan** cmdlet creates a recovery plan in Azure Site Recovery.</span></span>

<span data-ttu-id="75715-107">Ein Wiederherstellungsplan sammelt virtuelle Computer in einer Gruppe, um Failover und Wiederherstellung zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="75715-107">A recovery plan gathers virtual machines in a group for the purposes of failover and recovery.</span></span>

## <span data-ttu-id="75715-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="75715-108">EXAMPLES</span></span>

### <span data-ttu-id="75715-109">Beispiel 1: Hinzufügen eines Wiederherstellungsplans zu einem Website Wiederherstellungs Tresor</span><span class="sxs-lookup"><span data-stu-id="75715-109">Example 1: Add a recovery plan to a Site Recovery vault</span></span>
```
PS C:\> New-AzureSiteRecoveryRecoveryPlan -File "C:\Users\Contoso\Desktop\RecoveryPlan.xml"
```

<span data-ttu-id="75715-110">Mit diesem Befehl wird der Wiederherstellungsplan mit dem Namen RecoveryPlan.xml zum Azure Site Recovery Vault hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="75715-110">This command adds the recovery plan named RecoveryPlan.xml to the Azure Site Recovery vault.</span></span>

## <span data-ttu-id="75715-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="75715-111">PARAMETERS</span></span>

### <span data-ttu-id="75715-112">-Datei</span><span class="sxs-lookup"><span data-stu-id="75715-112">-File</span></span>
<span data-ttu-id="75715-113">Gibt den Pfad der Wiederherstellungsplan Datei an.</span><span class="sxs-lookup"><span data-stu-id="75715-113">Specifies the path of the recovery plan file.</span></span>

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

### <span data-ttu-id="75715-114">-Profil</span><span class="sxs-lookup"><span data-stu-id="75715-114">-Profile</span></span>
<span data-ttu-id="75715-115">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="75715-115">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="75715-116">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="75715-116">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="75715-117">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="75715-117">-WaitForCompletion</span></span>
<span data-ttu-id="75715-118">Gibt an, dass das Cmdlet wartet, bis der Vorgang abgeschlossen ist, bevor es die Steuerung an die Windows PowerShell-Konsole zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="75715-118">Indicates that the cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75715-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75715-119">CommonParameters</span></span>
<span data-ttu-id="75715-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75715-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75715-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75715-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75715-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="75715-122">INPUTS</span></span>

## <span data-ttu-id="75715-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="75715-123">OUTPUTS</span></span>

## <span data-ttu-id="75715-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="75715-124">NOTES</span></span>

## <span data-ttu-id="75715-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="75715-125">RELATED LINKS</span></span>

[<span data-ttu-id="75715-126">Get-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="75715-126">Get-AzureSiteRecoveryRecoveryPlan</span></span>](./Get-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="75715-127">Remove-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="75715-127">Remove-AzureSiteRecoveryRecoveryPlan</span></span>](./Remove-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="75715-128">Update-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="75715-128">Update-AzureSiteRecoveryRecoveryPlan</span></span>](./Update-AzureSiteRecoveryRecoveryPlan.md)



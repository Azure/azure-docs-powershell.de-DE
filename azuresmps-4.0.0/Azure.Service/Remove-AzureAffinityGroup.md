---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 29602F63-A05B-45AF-8DD8-5EBBF4C33FCE
online version: ''
schema: 2.0.0
ms.openlocfilehash: 32af8d2e89c14b0d36265efc688a88858851bba5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006378"
---
# <span data-ttu-id="8d8dc-101">Remove-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="8d8dc-101">Remove-AzureAffinityGroup</span></span>

## <span data-ttu-id="8d8dc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8d8dc-102">SYNOPSIS</span></span>
<span data-ttu-id="8d8dc-103">Löscht eine affinitätsgruppe in einem Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8d8dc-103">Deletes an affinity group in a subscription.</span></span>

## <span data-ttu-id="8d8dc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8d8dc-104">SYNTAX</span></span>

```
Remove-AzureAffinityGroup [-Name] <String> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="8d8dc-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8d8dc-105">DESCRIPTION</span></span>
<span data-ttu-id="8d8dc-106">Das Cmdlet **Remove-AzureAffinityGroup** löscht eine Azure-affinitätsgruppe im aktuellen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8d8dc-106">The **Remove-AzureAffinityGroup** cmdlet deletes an Azure affinity group in the current subscription.</span></span>
<span data-ttu-id="8d8dc-107">Eine affinitätsgruppe mit Mitgliedern kann nicht gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="8d8dc-107">You cannot delete an affinity group that has any members.</span></span>
<span data-ttu-id="8d8dc-108">Sie müssen zuerst alle Mitglieder einer affinitätsgruppe löschen.</span><span class="sxs-lookup"><span data-stu-id="8d8dc-108">You must first delete all the members of an affinity group.</span></span>

## <span data-ttu-id="8d8dc-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8d8dc-109">EXAMPLES</span></span>

### <span data-ttu-id="8d8dc-110">Beispiel 1: Entfernen einer affinitätsgruppe</span><span class="sxs-lookup"><span data-stu-id="8d8dc-110">Example 1: Remove an affinity group</span></span>
```
PS C:\> Remove-AzureAffinityGroup -Name "South01"
```

<span data-ttu-id="8d8dc-111">Dieser Befehl löscht die South01-affinitätsgruppe im aktuellen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8d8dc-111">This command deletes the South01 affinity group in the current subscription.</span></span>

## <span data-ttu-id="8d8dc-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="8d8dc-112">PARAMETERS</span></span>

### <span data-ttu-id="8d8dc-113">-Information</span><span class="sxs-lookup"><span data-stu-id="8d8dc-113">-InformationAction</span></span>
<span data-ttu-id="8d8dc-114">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="8d8dc-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="8d8dc-115">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="8d8dc-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8d8dc-116">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="8d8dc-116">Continue</span></span>
- <span data-ttu-id="8d8dc-117">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="8d8dc-117">Ignore</span></span>
- <span data-ttu-id="8d8dc-118">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="8d8dc-118">Inquire</span></span>
- <span data-ttu-id="8d8dc-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="8d8dc-119">SilentlyContinue</span></span>
- <span data-ttu-id="8d8dc-120">Beenden</span><span class="sxs-lookup"><span data-stu-id="8d8dc-120">Stop</span></span>
- <span data-ttu-id="8d8dc-121">Anhalten</span><span class="sxs-lookup"><span data-stu-id="8d8dc-121">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d8dc-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="8d8dc-122">-InformationVariable</span></span>
<span data-ttu-id="8d8dc-123">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="8d8dc-123">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d8dc-124">-Name</span><span class="sxs-lookup"><span data-stu-id="8d8dc-124">-Name</span></span>
<span data-ttu-id="8d8dc-125">Gibt den Namen der affinitätsgruppe an, die dieses Cmdlet löscht.</span><span class="sxs-lookup"><span data-stu-id="8d8dc-125">Specifies the name of the affinity group that this cmdlet deletes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d8dc-126">-Profil</span><span class="sxs-lookup"><span data-stu-id="8d8dc-126">-Profile</span></span>
<span data-ttu-id="8d8dc-127">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="8d8dc-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8d8dc-128">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="8d8dc-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8d8dc-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d8dc-129">CommonParameters</span></span>
<span data-ttu-id="8d8dc-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d8dc-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d8dc-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d8dc-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d8dc-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8d8dc-132">INPUTS</span></span>

## <span data-ttu-id="8d8dc-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8d8dc-133">OUTPUTS</span></span>

## <span data-ttu-id="8d8dc-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="8d8dc-134">NOTES</span></span>

## <span data-ttu-id="8d8dc-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8d8dc-135">RELATED LINKS</span></span>

[<span data-ttu-id="8d8dc-136">Get-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="8d8dc-136">Get-AzureAffinityGroup</span></span>](./Get-AzureAffinityGroup.md)

[<span data-ttu-id="8d8dc-137">Neu – AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="8d8dc-137">New-AzureAffinityGroup</span></span>](./New-AzureAffinityGroup.md)

[<span data-ttu-id="8d8dc-138">Satz-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="8d8dc-138">Set-AzureAffinityGroup</span></span>](./Set-AzureAffinityGroup.md)



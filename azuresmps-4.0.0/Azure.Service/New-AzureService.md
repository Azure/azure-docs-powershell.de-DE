---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: BB216903-B2BB-4948-AC28-408ED6C768F2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6cae249f99282006ff8636e8d727485a223e2a1d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006105"
---
# <span data-ttu-id="a94d5-101">New-AzureService</span><span class="sxs-lookup"><span data-stu-id="a94d5-101">New-AzureService</span></span>

## <span data-ttu-id="a94d5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a94d5-102">SYNOPSIS</span></span>
<span data-ttu-id="a94d5-103">Erstellt einen Azure-Dienst.</span><span class="sxs-lookup"><span data-stu-id="a94d5-103">Creates an Azure service.</span></span>

## <span data-ttu-id="a94d5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a94d5-104">SYNTAX</span></span>

### <span data-ttu-id="a94d5-105">ParameterSetAffinityGroup (Standard)</span><span class="sxs-lookup"><span data-stu-id="a94d5-105">ParameterSetAffinityGroup (Default)</span></span>
```
New-AzureService [-ServiceName] <String> [-AffinityGroup] <String> [[-Label] <String>]
 [[-Description] <String>] [[-ReverseDnsFqdn] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="a94d5-106">ParameterSetLocation</span><span class="sxs-lookup"><span data-stu-id="a94d5-106">ParameterSetLocation</span></span>
```
New-AzureService [-ServiceName] <String> [-Location] <String> [[-Label] <String>] [[-Description] <String>]
 [[-ReverseDnsFqdn] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="a94d5-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a94d5-107">DESCRIPTION</span></span>
<span data-ttu-id="a94d5-108">Das Cmdlet **New-AzureService** erstellt einen neuen Azure-Dienst im aktuellen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a94d5-108">The **New-AzureService** cmdlet creates a new Azure service in the current subscription.</span></span>

## <span data-ttu-id="a94d5-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a94d5-109">EXAMPLES</span></span>

### <span data-ttu-id="a94d5-110">Beispiel 1: Erstellen eines Diensts</span><span class="sxs-lookup"><span data-stu-id="a94d5-110">Example 1: Create a service</span></span>
```
PS C:\> New-AzureService -ServiceName "MySvc01" -Label "MyTestService" -Location "South Central US"
```

<span data-ttu-id="a94d5-111">Dieser Befehl erstellt einen neuen Dienst mit dem Namen "MySvc01" im Süd-Zentral-US-Standort.</span><span class="sxs-lookup"><span data-stu-id="a94d5-111">This command creates a new service named MySvc01 in the South Central US location.</span></span>

### <span data-ttu-id="a94d5-112">Beispiel 2: Erstellen eines Diensts in einer affinitätsgruppe</span><span class="sxs-lookup"><span data-stu-id="a94d5-112">Example 2: Create a service in an affinity group</span></span>
```
PS C:\> New-AzureService -ServiceName "MySvc01" -AffinityGroup NorthRegion
```

<span data-ttu-id="a94d5-113">Dieser Befehl erstellt mithilfe der NorthRegion-affinitätsgruppe einen neuen Dienst mit dem Namen MySvc01.</span><span class="sxs-lookup"><span data-stu-id="a94d5-113">This command creates a new service named MySvc01 using the NorthRegion affinity group.</span></span>

## <span data-ttu-id="a94d5-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="a94d5-114">PARAMETERS</span></span>

### <span data-ttu-id="a94d5-115">-Affinitygroup</span><span class="sxs-lookup"><span data-stu-id="a94d5-115">-AffinityGroup</span></span>
<span data-ttu-id="a94d5-116">Gibt die dem Abonnement zugeordnete affinitätsgruppe an.</span><span class="sxs-lookup"><span data-stu-id="a94d5-116">Specifies the affinity group associated with the subscription.</span></span>
<span data-ttu-id="a94d5-117">Wenn Sie den Parameter *Location* nicht angeben, ist eine affinitätsgruppe erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a94d5-117">If you do not specify the *Location* parameter, an affinity group is required.</span></span>

```yaml
Type: String
Parameter Sets: ParameterSetAffinityGroup
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a94d5-118">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a94d5-118">-Description</span></span>
<span data-ttu-id="a94d5-119">Gibt eine Beschreibung für den Dienst an.</span><span class="sxs-lookup"><span data-stu-id="a94d5-119">Specifies a description for the service.</span></span>
<span data-ttu-id="a94d5-120">Die Beschreibung kann bis zu 1024 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="a94d5-120">The description may be up to 1024 characters in length.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a94d5-121">-Information</span><span class="sxs-lookup"><span data-stu-id="a94d5-121">-InformationAction</span></span>
<span data-ttu-id="a94d5-122">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="a94d5-122">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="a94d5-123">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="a94d5-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a94d5-124">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="a94d5-124">Continue</span></span>
- <span data-ttu-id="a94d5-125">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="a94d5-125">Ignore</span></span>
- <span data-ttu-id="a94d5-126">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="a94d5-126">Inquire</span></span>
- <span data-ttu-id="a94d5-127">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="a94d5-127">SilentlyContinue</span></span>
- <span data-ttu-id="a94d5-128">Beenden</span><span class="sxs-lookup"><span data-stu-id="a94d5-128">Stop</span></span>
- <span data-ttu-id="a94d5-129">Anhalten</span><span class="sxs-lookup"><span data-stu-id="a94d5-129">Suspend</span></span>

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

### <span data-ttu-id="a94d5-130">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="a94d5-130">-InformationVariable</span></span>
<span data-ttu-id="a94d5-131">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="a94d5-131">Specifies an information variable.</span></span>

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

### <span data-ttu-id="a94d5-132">-Label</span><span class="sxs-lookup"><span data-stu-id="a94d5-132">-Label</span></span>
<span data-ttu-id="a94d5-133">Gibt eine Bezeichnung für den Dienst an.</span><span class="sxs-lookup"><span data-stu-id="a94d5-133">Specifies a label for the service.</span></span>
<span data-ttu-id="a94d5-134">Die Beschriftung kann bis zu 100 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="a94d5-134">The label may be up to 100 characters in length.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a94d5-135">-Standort</span><span class="sxs-lookup"><span data-stu-id="a94d5-135">-Location</span></span>
<span data-ttu-id="a94d5-136">Gibt den Standort des Diensts an.</span><span class="sxs-lookup"><span data-stu-id="a94d5-136">Specifies the location for the service.</span></span>
<span data-ttu-id="a94d5-137">Eine Position ist erforderlich, wenn keine angegebene affinitätsgruppe vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="a94d5-137">A location is required if there isn't a specified Affinity Group.</span></span>

```yaml
Type: String
Parameter Sets: ParameterSetLocation
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a94d5-138">-Profil</span><span class="sxs-lookup"><span data-stu-id="a94d5-138">-Profile</span></span>
<span data-ttu-id="a94d5-139">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="a94d5-139">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a94d5-140">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="a94d5-140">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a94d5-141">-ReverseDnsFqdn</span><span class="sxs-lookup"><span data-stu-id="a94d5-141">-ReverseDnsFqdn</span></span>
<span data-ttu-id="a94d5-142">Gibt den vollqualifizierten Domänennamen für Reverse-DNS an.</span><span class="sxs-lookup"><span data-stu-id="a94d5-142">Specifies the fully qualified domain name for reverse DNS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a94d5-143">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="a94d5-143">-ServiceName</span></span>
<span data-ttu-id="a94d5-144">Gibt den Namen des neuen Diensts an.</span><span class="sxs-lookup"><span data-stu-id="a94d5-144">Specifies the name of the new service.</span></span>
<span data-ttu-id="a94d5-145">Der Name muss für das Abonnement eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="a94d5-145">The name must be unique to the subscription.</span></span>

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

### <span data-ttu-id="a94d5-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a94d5-146">CommonParameters</span></span>
<span data-ttu-id="a94d5-147">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a94d5-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a94d5-148">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a94d5-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a94d5-149">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a94d5-149">INPUTS</span></span>

## <span data-ttu-id="a94d5-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a94d5-150">OUTPUTS</span></span>

## <span data-ttu-id="a94d5-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="a94d5-151">NOTES</span></span>

## <span data-ttu-id="a94d5-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a94d5-152">RELATED LINKS</span></span>

[<span data-ttu-id="a94d5-153">Get-AzureService</span><span class="sxs-lookup"><span data-stu-id="a94d5-153">Get-AzureService</span></span>](./Get-AzureService.md)

[<span data-ttu-id="a94d5-154">Satz-AzureService</span><span class="sxs-lookup"><span data-stu-id="a94d5-154">Set-AzureService</span></span>](./Set-AzureService.md)



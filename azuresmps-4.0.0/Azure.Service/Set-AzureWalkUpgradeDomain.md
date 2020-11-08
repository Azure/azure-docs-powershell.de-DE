---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 3F3BC5AF-8D7B-40BF-A072-A11C7BDCB6B3
online version: ''
schema: 2.0.0
ms.openlocfilehash: 09adc7e9b2faf9b9a905fa1c94fb6526e02c110f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005992"
---
# <span data-ttu-id="4a661-101">Set-AzureWalkUpgradeDomain</span><span class="sxs-lookup"><span data-stu-id="4a661-101">Set-AzureWalkUpgradeDomain</span></span>

## <span data-ttu-id="4a661-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4a661-102">SYNOPSIS</span></span>
<span data-ttu-id="4a661-103">Führt die angegebene Upgrade-Domäne durch.</span><span class="sxs-lookup"><span data-stu-id="4a661-103">Walks the specified upgrade domain.</span></span>

## <span data-ttu-id="4a661-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4a661-104">SYNTAX</span></span>

```
Set-AzureWalkUpgradeDomain [-ServiceName] <String> [-Slot] <String> [-DomainNumber] <Int32>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="4a661-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4a661-105">DESCRIPTION</span></span>
<span data-ttu-id="4a661-106">Das Cmdlet " **Satz-AzureWalkUpgradeDomain** " initiiert das eigentliche Upgrade einer Azure-Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="4a661-106">The **Set-AzureWalkUpgradeDomain** cmdlet initiates the actual upgrade of an Azure deployment.</span></span>
<span data-ttu-id="4a661-107">Das Upgrade-Paket und die Konfiguration werden mithilfe des Cmdlets " **Set-AzureDeployment** " mit dem Schalter "-Upgrade" eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="4a661-107">The upgrade package and configuration are set by using the **Set-AzureDeployment** cmdlet with the -Upgrade switch.</span></span>

## <span data-ttu-id="4a661-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4a661-108">EXAMPLES</span></span>

### <span data-ttu-id="4a661-109">Beispiel 1: Initiieren eines Upgrades einer Produktionsbereitstellung</span><span class="sxs-lookup"><span data-stu-id="4a661-109">Example 1: Initiate an upgrade of a production deployment</span></span>
```
PS C:\> Set-AzureWalkUpgradeDomain -ServiceName "MySvc1" -slot "Production" -UpgradeDomain 2
```

<span data-ttu-id="4a661-110">Mit diesem Befehl wird das Upgrade der Upgrade-Domäne 2 der Produktionsbereitstellung des MySvc1-Diensts initiiert.</span><span class="sxs-lookup"><span data-stu-id="4a661-110">This command initiates the upgrade of Upgrade Domain 2 of the production deployment of the MySvc1 service.</span></span>

## <span data-ttu-id="4a661-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="4a661-111">PARAMETERS</span></span>

### <span data-ttu-id="4a661-112">-DomainNumber</span><span class="sxs-lookup"><span data-stu-id="4a661-112">-DomainNumber</span></span>
<span data-ttu-id="4a661-113">Gibt die Upgrade-Domäne an, die aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="4a661-113">Specifies the upgrade domain to upgrade.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a661-114">-Information</span><span class="sxs-lookup"><span data-stu-id="4a661-114">-InformationAction</span></span>
<span data-ttu-id="4a661-115">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="4a661-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="4a661-116">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="4a661-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4a661-117">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="4a661-117">Continue</span></span>
- <span data-ttu-id="4a661-118">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="4a661-118">Ignore</span></span>
- <span data-ttu-id="4a661-119">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="4a661-119">Inquire</span></span>
- <span data-ttu-id="4a661-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="4a661-120">SilentlyContinue</span></span>
- <span data-ttu-id="4a661-121">Beenden</span><span class="sxs-lookup"><span data-stu-id="4a661-121">Stop</span></span>
- <span data-ttu-id="4a661-122">Anhalten</span><span class="sxs-lookup"><span data-stu-id="4a661-122">Suspend</span></span>

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

### <span data-ttu-id="4a661-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="4a661-123">-InformationVariable</span></span>
<span data-ttu-id="4a661-124">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="4a661-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="4a661-125">-Profil</span><span class="sxs-lookup"><span data-stu-id="4a661-125">-Profile</span></span>
<span data-ttu-id="4a661-126">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="4a661-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4a661-127">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="4a661-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4a661-128">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="4a661-128">-ServiceName</span></span>
<span data-ttu-id="4a661-129">Gibt den Namen des Microsoft Azure-Diensts an, der aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="4a661-129">Specifies the Microsoft Azure service name to upgrade.</span></span>

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

### <span data-ttu-id="4a661-130">-Slot</span><span class="sxs-lookup"><span data-stu-id="4a661-130">-Slot</span></span>
<span data-ttu-id="4a661-131">Gibt die Umgebung der Bereitstellung an, die aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="4a661-131">Specifies the environment of the deployment to upgrade.</span></span>

<span data-ttu-id="4a661-132">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="4a661-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4a661-133">Inszenierung</span><span class="sxs-lookup"><span data-stu-id="4a661-133">Staging</span></span>
- <span data-ttu-id="4a661-134">Produktions</span><span class="sxs-lookup"><span data-stu-id="4a661-134">Production</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a661-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a661-135">CommonParameters</span></span>
<span data-ttu-id="4a661-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a661-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a661-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a661-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a661-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4a661-138">INPUTS</span></span>

## <span data-ttu-id="4a661-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4a661-139">OUTPUTS</span></span>

### <span data-ttu-id="4a661-140">ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="4a661-140">ManagementOperationContext</span></span>

## <span data-ttu-id="4a661-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="4a661-141">NOTES</span></span>

## <span data-ttu-id="4a661-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4a661-142">RELATED LINKS</span></span>

[<span data-ttu-id="4a661-143">Satz-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="4a661-143">Set-AzureDeployment</span></span>](./Set-AzureDeployment.md)



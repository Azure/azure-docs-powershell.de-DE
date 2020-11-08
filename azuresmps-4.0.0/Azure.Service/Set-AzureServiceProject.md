---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D0A2B454-7BFF-4D4D-8A85-FDB47249758F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5f4d1598f17629d178e1feff1b5549631be48c60
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006025"
---
# <span data-ttu-id="583b8-101">Set-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="583b8-101">Set-AzureServiceProject</span></span>

## <span data-ttu-id="583b8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="583b8-102">SYNOPSIS</span></span>
<span data-ttu-id="583b8-103">Legt den Standardstandort, das Abonnement, den Steckplatz und das Speicherkonto für den aktuellen Dienst fest.</span><span class="sxs-lookup"><span data-stu-id="583b8-103">Sets default location, subscription, slot, and storage account for the current service.</span></span>

## <span data-ttu-id="583b8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="583b8-104">SYNTAX</span></span>

```
Set-AzureServiceProject [-Location <String>] [-Slot <String>] [-Storage <String>] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="583b8-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="583b8-105">DESCRIPTION</span></span>
<span data-ttu-id="583b8-106">Das Cmdlet " **Set-AzureServiceProject** " legt den Bereitstellungsspeicherort, den Steckplatz, das Speicherkonto und das Abonnement für den aktuellen Dienst fest.</span><span class="sxs-lookup"><span data-stu-id="583b8-106">The **Set-AzureServiceProject** cmdlet sets the deployment location, slot, storage account, and subscription for the current service.</span></span>
<span data-ttu-id="583b8-107">Diese Werte werden immer dann verwendet, wenn der Dienst in der Cloud veröffentlicht wird.</span><span class="sxs-lookup"><span data-stu-id="583b8-107">These values are used whenever the service is published to the cloud.</span></span>

## <span data-ttu-id="583b8-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="583b8-108">EXAMPLES</span></span>

### <span data-ttu-id="583b8-109">Beispiel 1: grundlegende Einstellungen</span><span class="sxs-lookup"><span data-stu-id="583b8-109">Example 1: Basic settings</span></span>
```
PS C:\> Set-AzureServiceProject -Location "North Central US" -Slot Production -Storage myStorageAccount -Subscription myAzureSubscription
```

<span data-ttu-id="583b8-110">Legt den Bereitstellungsspeicherort für den Dienst auf die Nord zentrale US-Region fest.</span><span class="sxs-lookup"><span data-stu-id="583b8-110">Sets the deployment location for the service to the North Central US region.</span></span>
<span data-ttu-id="583b8-111">Legt den Bereitstellungs Steckplatz auf Production fest.</span><span class="sxs-lookup"><span data-stu-id="583b8-111">Sets the deployment slot to Production.</span></span> <span data-ttu-id="583b8-112">Legt das Speicherkonto fest, das zum Bereitstellen der Dienstdefinition für myStorageAccount verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="583b8-112">Sets the storage account that will be used to stage the service definition to myStorageAccount.</span></span>
<span data-ttu-id="583b8-113">Legt das Abonnement fest, das den Dienst für mysubscription hosten soll.</span><span class="sxs-lookup"><span data-stu-id="583b8-113">Sets the subscription that will host the service to mySubscription.</span></span>
<span data-ttu-id="583b8-114">Wenn der Dienst in der Cloud veröffentlicht wird, wird er in einem Rechenzentrum in der Region Nord-Zentralamerika gehostet, der Bereitstellungs Steckplatz wird aktualisiert, und es wird das angegebene Abonnement-und Speicherkonto verwendet.</span><span class="sxs-lookup"><span data-stu-id="583b8-114">Whenever the service is published to the cloud, it will be hosted in a data center in the North Central US region, it will update the deployment slot, and it will use the specified subscription and storage account.</span></span>

## <span data-ttu-id="583b8-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="583b8-115">PARAMETERS</span></span>

### <span data-ttu-id="583b8-116">-Standort</span><span class="sxs-lookup"><span data-stu-id="583b8-116">-Location</span></span>
<span data-ttu-id="583b8-117">Der Bereich, in dem der Dienst gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="583b8-117">The region in which the service will be hosted.</span></span>
<span data-ttu-id="583b8-118">Dieser Wert wird immer dann verwendet, wenn der Dienst in der Cloud veröffentlicht wird.</span><span class="sxs-lookup"><span data-stu-id="583b8-118">This value is used whenever the service is published to the cloud.</span></span>
<span data-ttu-id="583b8-119">Mögliche Werte sind: überall in Asien, überall in Europa, überall in den USA, Ostasien, Ost-und Nordamerika, Nordeuropa, Süd-Zentralamerika, Südostasien, Westeuropa, Westamerika.</span><span class="sxs-lookup"><span data-stu-id="583b8-119">Possible values are: Anywhere Asia, Anywhere Europe, Anywhere US, East Asia, East US, North Central US, North Europe, South Central US, Southeast Asia, West Europe, West US.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="583b8-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="583b8-120">-PassThru</span></span>
<span data-ttu-id="583b8-121">Gibt an, dass dieses Cmdlet ein Objekt zurückgibt, das das Element darstellt, auf dem es ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="583b8-121">Indicates that this cmdlet returns an object representing the item on which it operates.</span></span>
<span data-ttu-id="583b8-122">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="583b8-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="583b8-123">-Profil</span><span class="sxs-lookup"><span data-stu-id="583b8-123">-Profile</span></span>
<span data-ttu-id="583b8-124">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="583b8-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="583b8-125">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="583b8-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="583b8-126">-Slot</span><span class="sxs-lookup"><span data-stu-id="583b8-126">-Slot</span></span>
<span data-ttu-id="583b8-127">Der Slot (Production oder Staging), in dem der Dienst gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="583b8-127">The slot (production or staging) in which the service will be hosted.</span></span>
<span data-ttu-id="583b8-128">Dieser Wert wird immer dann verwendet, wenn der Dienst in der Cloud veröffentlicht wird.</span><span class="sxs-lookup"><span data-stu-id="583b8-128">This value is used whenever the service is published to the cloud.</span></span>
<span data-ttu-id="583b8-129">Mögliche Werte sind: Production, Staging.</span><span class="sxs-lookup"><span data-stu-id="583b8-129">Possible values are: Production, Staging.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="583b8-130">-Speicher</span><span class="sxs-lookup"><span data-stu-id="583b8-130">-Storage</span></span>
<span data-ttu-id="583b8-131">Das Speicherkonto, das beim Hochladen des Dienstpakets in die Cloud verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="583b8-131">The storage account to be used when uploading the service package to the cloud.</span></span>
<span data-ttu-id="583b8-132">Wenn das Speicherkonto nicht vorhanden ist, wird es erstellt, wenn der Dienst in der Cloud veröffentlicht wird.</span><span class="sxs-lookup"><span data-stu-id="583b8-132">If the storage account doesn't exist, it will be created when the service is published to the cloud.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="583b8-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="583b8-133">CommonParameters</span></span>
<span data-ttu-id="583b8-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="583b8-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="583b8-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="583b8-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="583b8-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="583b8-136">INPUTS</span></span>

## <span data-ttu-id="583b8-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="583b8-137">OUTPUTS</span></span>

## <span data-ttu-id="583b8-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="583b8-138">NOTES</span></span>
* <span data-ttu-id="583b8-139">Node-dev, php-dev, python-dev</span><span class="sxs-lookup"><span data-stu-id="583b8-139">node-dev, php-dev, python-dev</span></span>

## <span data-ttu-id="583b8-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="583b8-140">RELATED LINKS</span></span>

[<span data-ttu-id="583b8-141">Neu – AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="583b8-141">New-AzureServiceProject</span></span>](./New-AzureServiceProject.md)

[<span data-ttu-id="583b8-142">Publish-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="583b8-142">Publish-AzureServiceProject</span></span>](./Publish-AzureServiceProject.md)

[<span data-ttu-id="583b8-143">Satz-AzureServiceProjectRole</span><span class="sxs-lookup"><span data-stu-id="583b8-143">Set-AzureServiceProjectRole</span></span>](./Set-AzureServiceProjectRole.md)



---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 793037C4-8FE5-4799-B59B-94C1605D9F4E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 593ea36e90635472db1f8568254657f782bd1200
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006407"
---
# <span data-ttu-id="c4064-101">New-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="c4064-101">New-AzureStoreAddOn</span></span>

## <span data-ttu-id="c4064-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c4064-102">SYNOPSIS</span></span>
<span data-ttu-id="c4064-103">Kauft eine neue Add-on-Instanz.</span><span class="sxs-lookup"><span data-stu-id="c4064-103">Buys a new add-on instance.</span></span>

## <span data-ttu-id="c4064-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c4064-104">SYNTAX</span></span>

```
New-AzureStoreAddOn -Name <String> -AddOn <String> -Plan <String> -Location <String> [-PromotionCode <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c4064-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c4064-105">DESCRIPTION</span></span>
<span data-ttu-id="c4064-106">In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c4064-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="c4064-107">Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="c4064-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="c4064-108">Kauft eine neue Add-on-Instanz aus dem Azure Store.</span><span class="sxs-lookup"><span data-stu-id="c4064-108">Buys a new add-on instance from the Azure Store.</span></span>

## <span data-ttu-id="c4064-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c4064-109">EXAMPLES</span></span>

### <span data-ttu-id="c4064-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c4064-110">Example 1</span></span>
```
PS C:\> New-AzureStoreAddOn -Name MyAddOn -AddOn AddonId -Plan PlanId -Location "West US"
```

<span data-ttu-id="c4064-111">In diesem Beispiel wird ein Add-on mit dem Namen myaddon mit einer Planwert in West US-Position gekauft.</span><span class="sxs-lookup"><span data-stu-id="c4064-111">This example buys an add-on named MyAddOn with a PlanId in West US location.</span></span>

### <span data-ttu-id="c4064-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="c4064-112">Example 2</span></span>
```
PS C:\> New-AzureStoreAddOn -Name MyAddOn -AddOn AddonId -Plan PlanId -Location "West US" -PromotionCode MyPromoCode
```

<span data-ttu-id="c4064-113">In diesem Beispiel wird ein Werbe Code verwendet, um ein Add-on zu kaufen.</span><span class="sxs-lookup"><span data-stu-id="c4064-113">This example uses a promotional code to buy an add-on.</span></span>

## <span data-ttu-id="c4064-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="c4064-114">PARAMETERS</span></span>

### <span data-ttu-id="c4064-115">-Addon</span><span class="sxs-lookup"><span data-stu-id="c4064-115">-AddOn</span></span>
<span data-ttu-id="c4064-116">Gibt die Add-on-ID an.</span><span class="sxs-lookup"><span data-stu-id="c4064-116">Specifies the add-on ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4064-117">-Standort</span><span class="sxs-lookup"><span data-stu-id="c4064-117">-Location</span></span>
<span data-ttu-id="c4064-118">Gibt den Speicherort der Add-on-Instanz an.</span><span class="sxs-lookup"><span data-stu-id="c4064-118">Specifies the add-on instance location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4064-119">-Name</span><span class="sxs-lookup"><span data-stu-id="c4064-119">-Name</span></span>
<span data-ttu-id="c4064-120">Gibt den Namen der Add-on-Instanz an.</span><span class="sxs-lookup"><span data-stu-id="c4064-120">Specifies the name of the add-on instance.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4064-121">-Plan</span><span class="sxs-lookup"><span data-stu-id="c4064-121">-Plan</span></span>
<span data-ttu-id="c4064-122">Gibt die Plan-ID an.</span><span class="sxs-lookup"><span data-stu-id="c4064-122">Specifies the plan ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4064-123">-Profil</span><span class="sxs-lookup"><span data-stu-id="c4064-123">-Profile</span></span>
<span data-ttu-id="c4064-124">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="c4064-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c4064-125">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="c4064-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c4064-126">-PromotionCode</span><span class="sxs-lookup"><span data-stu-id="c4064-126">-PromotionCode</span></span>
<span data-ttu-id="c4064-127">Gibt einen Werbe Code an, der für den Kauf gelten soll.</span><span class="sxs-lookup"><span data-stu-id="c4064-127">Specifies a promotion code to apply to the purchase.</span></span>

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

### <span data-ttu-id="c4064-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4064-128">CommonParameters</span></span>
<span data-ttu-id="c4064-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4064-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4064-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4064-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4064-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c4064-131">INPUTS</span></span>

## <span data-ttu-id="c4064-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c4064-132">OUTPUTS</span></span>

## <span data-ttu-id="c4064-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="c4064-133">NOTES</span></span>

## <span data-ttu-id="c4064-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c4064-134">RELATED LINKS</span></span>

[<span data-ttu-id="c4064-135">Get-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="c4064-135">Get-AzureStoreAddOn</span></span>](./Get-AzureStoreAddOn.md)

[<span data-ttu-id="c4064-136">Remove-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="c4064-136">Remove-AzureStoreAddOn</span></span>](./Remove-AzureStoreAddOn.md)

[<span data-ttu-id="c4064-137">Satz-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="c4064-137">Set-AzureStoreAddOn</span></span>](./Set-AzureStoreAddOn.md)



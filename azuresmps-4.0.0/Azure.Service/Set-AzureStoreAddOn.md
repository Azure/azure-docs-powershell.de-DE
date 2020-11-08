---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: F5EC8E00-E504-436A-96FF-4E886579AEA4
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5b72fcfac0b000a8fcfc11dbab6961460cb25b8b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006621"
---
# <span data-ttu-id="37878-101">Set-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="37878-101">Set-AzureStoreAddOn</span></span>

## <span data-ttu-id="37878-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="37878-102">SYNOPSIS</span></span>
<span data-ttu-id="37878-103">Aktualisiert eine vorhandene Add-on-Instanz.</span><span class="sxs-lookup"><span data-stu-id="37878-103">Updates an existing add-on instance.</span></span>

## <span data-ttu-id="37878-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="37878-104">SYNTAX</span></span>

```
Set-AzureStoreAddOn -Name <String> -Plan <String> [-PromotionCode <String>] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="37878-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="37878-105">DESCRIPTION</span></span>
<span data-ttu-id="37878-106">In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="37878-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="37878-107">Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="37878-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="37878-108">Dieses Cmdlet aktualisiert eine vorhandene Add-on-Instanz aus dem aktuellen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="37878-108">This cmdlet updates an existing add-on instance from the current subscription.</span></span>

## <span data-ttu-id="37878-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="37878-109">EXAMPLES</span></span>

### <span data-ttu-id="37878-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="37878-110">Example 1</span></span>
```
PS C:\> Set-AzureStoreAddOn MyAddOn NewPlanId
```

<span data-ttu-id="37878-111">In diesem Beispiel wird ein Add-on mit einer neuen Plan-ID aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="37878-111">This example updates an add-on with a new plan ID.</span></span>

### <span data-ttu-id="37878-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="37878-112">Example 2</span></span>
```
PS C:\> Set-AzureStoreAddOn MyAddOn NewPlanId MyPromoCode
```

<span data-ttu-id="37878-113">In diesem Beispiel wird ein Add-on mit einer neuen Plan-ID und einem Werbe Code aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="37878-113">This example updates an add-on with a new plan ID and promotional code.</span></span>

## <span data-ttu-id="37878-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="37878-114">PARAMETERS</span></span>

### <span data-ttu-id="37878-115">-Name</span><span class="sxs-lookup"><span data-stu-id="37878-115">-Name</span></span>
<span data-ttu-id="37878-116">Gibt den Namen der Add-on-Instanz an.</span><span class="sxs-lookup"><span data-stu-id="37878-116">Specifies the name of the add-on instance.</span></span>

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

### <span data-ttu-id="37878-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="37878-117">-PassThru</span></span>
<span data-ttu-id="37878-118">Wenn angegeben, gibt das Cmdlet true zurück, wenn der Befehl erfolgreich ist, und false, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="37878-118">If specified, the cmdlet returns true if the command succeeds and false if it fails.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37878-119">-Plan</span><span class="sxs-lookup"><span data-stu-id="37878-119">-Plan</span></span>
<span data-ttu-id="37878-120">Gibt die Plan-ID an.</span><span class="sxs-lookup"><span data-stu-id="37878-120">Specifies the plan ID.</span></span>

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

### <span data-ttu-id="37878-121">-Profil</span><span class="sxs-lookup"><span data-stu-id="37878-121">-Profile</span></span>
<span data-ttu-id="37878-122">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="37878-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="37878-123">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="37878-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="37878-124">-PromotionCode</span><span class="sxs-lookup"><span data-stu-id="37878-124">-PromotionCode</span></span>
<span data-ttu-id="37878-125">Gibt den Werbe Code an.</span><span class="sxs-lookup"><span data-stu-id="37878-125">Specifies the promotional code.</span></span>

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

### <span data-ttu-id="37878-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37878-126">CommonParameters</span></span>
<span data-ttu-id="37878-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37878-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37878-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37878-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37878-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="37878-129">INPUTS</span></span>

## <span data-ttu-id="37878-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="37878-130">OUTPUTS</span></span>

## <span data-ttu-id="37878-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="37878-131">NOTES</span></span>

## <span data-ttu-id="37878-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="37878-132">RELATED LINKS</span></span>

[<span data-ttu-id="37878-133">Get-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="37878-133">Get-AzureStoreAddOn</span></span>](./Get-AzureStoreAddOn.md)

[<span data-ttu-id="37878-134">Neu – AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="37878-134">New-AzureStoreAddOn</span></span>](./New-AzureStoreAddOn.md)

[<span data-ttu-id="37878-135">Remove-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="37878-135">Remove-AzureStoreAddOn</span></span>](./Remove-AzureStoreAddOn.md)



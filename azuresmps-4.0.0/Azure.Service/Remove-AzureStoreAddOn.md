---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D927B159-AD68-4071-ADE3-FA2430750D72
online version: ''
schema: 2.0.0
ms.openlocfilehash: 001466cb00ad15f1cbfef6dcf9fd3ce9b931109b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006661"
---
# <span data-ttu-id="bc262-101">Remove-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="bc262-101">Remove-AzureStoreAddOn</span></span>

## <span data-ttu-id="bc262-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bc262-102">SYNOPSIS</span></span>
<span data-ttu-id="bc262-103">Entfernt eine vorhandene Add-on-Instanz.</span><span class="sxs-lookup"><span data-stu-id="bc262-103">Removes an existing add-on instance.</span></span>

## <span data-ttu-id="bc262-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bc262-104">SYNTAX</span></span>

```
Remove-AzureStoreAddOn -Name <String> [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="bc262-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bc262-105">DESCRIPTION</span></span>
<span data-ttu-id="bc262-106">In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="bc262-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="bc262-107">Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="bc262-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="bc262-108">Entfernt eine vorhandene Add-on-Instanz aus dem aktuellen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="bc262-108">Removes an existing add-on instance from the current subscription.</span></span>

## <span data-ttu-id="bc262-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bc262-109">EXAMPLES</span></span>

### <span data-ttu-id="bc262-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="bc262-110">Example 1</span></span>
```
PS C:\> Remove-AzureStoreAddOn MyAddOn
```

<span data-ttu-id="bc262-111">In diesem Beispiel wird ein Add-on namens myaddon aus dem aktuellen Abonnement entfernt.</span><span class="sxs-lookup"><span data-stu-id="bc262-111">This example removes an add-on named MyAddOn from the current subscription.</span></span>

## <span data-ttu-id="bc262-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="bc262-112">PARAMETERS</span></span>

### <span data-ttu-id="bc262-113">-Name</span><span class="sxs-lookup"><span data-stu-id="bc262-113">-Name</span></span>
<span data-ttu-id="bc262-114">Gibt den Namen der Add-on-Instanz an, die entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="bc262-114">Specifies the name of the add-on instance to remove.</span></span>

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

### <span data-ttu-id="bc262-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bc262-115">-PassThru</span></span>
<span data-ttu-id="bc262-116">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="bc262-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="bc262-117">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="bc262-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="bc262-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="bc262-118">-Profile</span></span>
<span data-ttu-id="bc262-119">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="bc262-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="bc262-120">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="bc262-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="bc262-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc262-121">CommonParameters</span></span>
<span data-ttu-id="bc262-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc262-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc262-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc262-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc262-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bc262-124">INPUTS</span></span>

## <span data-ttu-id="bc262-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bc262-125">OUTPUTS</span></span>

## <span data-ttu-id="bc262-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="bc262-126">NOTES</span></span>

## <span data-ttu-id="bc262-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bc262-127">RELATED LINKS</span></span>

[<span data-ttu-id="bc262-128">Get-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="bc262-128">Get-AzureStoreAddOn</span></span>](./Get-AzureStoreAddOn.md)

[<span data-ttu-id="bc262-129">Neu – AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="bc262-129">New-AzureStoreAddOn</span></span>](./New-AzureStoreAddOn.md)

[<span data-ttu-id="bc262-130">Satz-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="bc262-130">Set-AzureStoreAddOn</span></span>](./Set-AzureStoreAddOn.md)



---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 61CF7F95-F0BB-4282-A971-537CB73708B1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3d5774213054f3e9e56e9804a9319e31f095f868
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005753"
---
# <span data-ttu-id="63968-101">Get-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="63968-101">Get-AzureStoreAddOn</span></span>

## <span data-ttu-id="63968-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="63968-102">SYNOPSIS</span></span>
<span data-ttu-id="63968-103">Ruft die verfügbaren Azure Store-Add-ons ab.</span><span class="sxs-lookup"><span data-stu-id="63968-103">Gets the available Azure Store add-ons.</span></span>

## <span data-ttu-id="63968-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="63968-104">SYNTAX</span></span>

### <span data-ttu-id="63968-105">ListAvailable</span><span class="sxs-lookup"><span data-stu-id="63968-105">ListAvailable</span></span>
```
Get-AzureStoreAddOn [-ListAvailable] [-Country <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="63968-106">Getaddon</span><span class="sxs-lookup"><span data-stu-id="63968-106">GetAddOn</span></span>
```
Get-AzureStoreAddOn [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="63968-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="63968-107">DESCRIPTION</span></span>
<span data-ttu-id="63968-108">In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="63968-108">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="63968-109">Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="63968-109">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="63968-110">Ruft alle verfügbaren Add-ons für den Kauf aus dem Azure Store ab oder ruft die vorhandenen Add-on-Instanzen für das aktuelle Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="63968-110">Gets all the available add-ons for purchasing from the Azure Store, or gets the existing add-on instances for the current subscription.</span></span>

## <span data-ttu-id="63968-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="63968-111">EXAMPLES</span></span>

### <span data-ttu-id="63968-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="63968-112">Example 1</span></span>
```
PS C:\> Get-AzureStoreAddOn
```

<span data-ttu-id="63968-113">In diesem Beispiel werden alle gekauften Add-on-Instanzen für das aktuelle Abonnement abgerufen.</span><span class="sxs-lookup"><span data-stu-id="63968-113">This example gets all purchased add-on instances for the current subscription.</span></span>

### <span data-ttu-id="63968-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="63968-114">Example 2</span></span>
```
PS C:\> Get-AzureStoreAddOn -ListAvailable
```

<span data-ttu-id="63968-115">In diesem Beispiel werden alle verfügbaren Add-ons für den Kauf in den Vereinigten Staaten aus dem Azure Store abgerufen.</span><span class="sxs-lookup"><span data-stu-id="63968-115">This example gets all the available add-ons for purchasing in United States from the Azure Store.</span></span>

### <span data-ttu-id="63968-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="63968-116">Example 3</span></span>
```
PS C:\> Get-AzureStoreAddOn -Name MyAddOn
```

<span data-ttu-id="63968-117">In diesem Beispiel wird ein Add-on mit dem Namen myaddon aus der gekauften Add-on-Instanz im aktuellen Abonnement abgerufen.</span><span class="sxs-lookup"><span data-stu-id="63968-117">This example gets an add-on named MyAddOn from the purchased add-on instance in the current subscription.</span></span>

## <span data-ttu-id="63968-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="63968-118">PARAMETERS</span></span>

### <span data-ttu-id="63968-119">-Land</span><span class="sxs-lookup"><span data-stu-id="63968-119">-Country</span></span>
<span data-ttu-id="63968-120">Gibt bei Angabe nur die im angegebenen Land verfügbaren Azure Store-Add-on-Instanzen zurück.</span><span class="sxs-lookup"><span data-stu-id="63968-120">If specified, returns only the Azure Store add-on instances available in the specified country.</span></span>
<span data-ttu-id="63968-121">Der Standardwert ist "US".</span><span class="sxs-lookup"><span data-stu-id="63968-121">The default is "US".</span></span>

```yaml
Type: String
Parameter Sets: ListAvailable
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63968-122">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="63968-122">-ListAvailable</span></span>
<span data-ttu-id="63968-123">Wenn angegeben, werden die verfügbaren Add-ons für den Kauf aus dem Azure Store abgerufen.</span><span class="sxs-lookup"><span data-stu-id="63968-123">If specified, gets available add-ons for purchasing from the Azure Store.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ListAvailable
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63968-124">-Name</span><span class="sxs-lookup"><span data-stu-id="63968-124">-Name</span></span>
<span data-ttu-id="63968-125">Gibt das Add-on zurück, das dem angegebenen Namen entspricht.</span><span class="sxs-lookup"><span data-stu-id="63968-125">Returns the add-on that matches the specified name.</span></span>

```yaml
Type: String
Parameter Sets: GetAddOn
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63968-126">-Profil</span><span class="sxs-lookup"><span data-stu-id="63968-126">-Profile</span></span>
<span data-ttu-id="63968-127">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="63968-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="63968-128">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="63968-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="63968-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63968-129">CommonParameters</span></span>
<span data-ttu-id="63968-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63968-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63968-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63968-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63968-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="63968-132">INPUTS</span></span>

## <span data-ttu-id="63968-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="63968-133">OUTPUTS</span></span>

## <span data-ttu-id="63968-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="63968-134">NOTES</span></span>

## <span data-ttu-id="63968-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="63968-135">RELATED LINKS</span></span>

[<span data-ttu-id="63968-136">Neu – AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="63968-136">New-AzureStoreAddOn</span></span>](./New-AzureStoreAddOn.md)

[<span data-ttu-id="63968-137">Remove-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="63968-137">Remove-AzureStoreAddOn</span></span>](./Remove-AzureStoreAddOn.md)

[<span data-ttu-id="63968-138">Satz-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="63968-138">Set-AzureStoreAddOn</span></span>](./Set-AzureStoreAddOn.md)



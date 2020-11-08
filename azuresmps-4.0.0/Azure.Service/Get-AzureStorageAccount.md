---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7D7D1FAE-5360-428B-AAE9-9D1109A7B67F
online version: ''
schema: 2.0.0
ms.openlocfilehash: faccd241929beca1f2423fa9c23f35793233205b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005755"
---
# <span data-ttu-id="869bc-101">Get-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="869bc-101">Get-AzureStorageAccount</span></span>

## <span data-ttu-id="869bc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="869bc-102">SYNOPSIS</span></span>
<span data-ttu-id="869bc-103">Ruft die Speicherkonten für das aktuelle Azure-Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="869bc-103">Gets the storage accounts for the current Azure subscription.</span></span>

## <span data-ttu-id="869bc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="869bc-104">SYNTAX</span></span>

```
Get-AzureStorageAccount [[-StorageAccountName] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="869bc-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="869bc-105">DESCRIPTION</span></span>
<span data-ttu-id="869bc-106">Das Cmdlet " **Get-AzureStorageAccount** " gibt ein Objekt zurück, das Informationen zu den Speicherkonten für das aktuelle Abonnement enthält.</span><span class="sxs-lookup"><span data-stu-id="869bc-106">The **Get-AzureStorageAccount** cmdlet returns an object containing information about the storage accounts for the current subscription.</span></span>
<span data-ttu-id="869bc-107">Wenn der Parameter *StorageAccountName* angegeben wird, werden nur Informationen über das angegebene Speicherkonto zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="869bc-107">If the *StorageAccountName* parameter is specified, then only information about the specified storage account is returned.</span></span>

## <span data-ttu-id="869bc-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="869bc-108">EXAMPLES</span></span>

### <span data-ttu-id="869bc-109">Beispiel 1: Zurückgeben aller Speicherkonten</span><span class="sxs-lookup"><span data-stu-id="869bc-109">Example 1: Return all storage accounts</span></span>
```
PS C:\> Get-AzureStorageAccount
```

<span data-ttu-id="869bc-110">Dieser Befehl gibt ein Objekt mit allen Speicherkonten zurück, die dem aktuellen Abonnement zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="869bc-110">This command returns an object with all the storage accounts associated with the current subscription.</span></span>

### <span data-ttu-id="869bc-111">Beispiel 2: Zurückgeben von Kontoinformationen für ein angegebenes Konto</span><span class="sxs-lookup"><span data-stu-id="869bc-111">Example 2: Return account information for a specified account</span></span>
```
PS C:\> Get-AzureStorageAccount -StorageAccountName "ContosoStore01"
```

<span data-ttu-id="869bc-112">Dieser Befehl gibt ein Objekt zurück, das nur die ContosoStore01-Kontoinformationen hat.</span><span class="sxs-lookup"><span data-stu-id="869bc-112">This command returns an object with only the ContosoStore01 account information.</span></span>

### <span data-ttu-id="869bc-113">Beispiel 3: Anzeigen einer Tabelle mit Speicherkonten</span><span class="sxs-lookup"><span data-stu-id="869bc-113">Example 3: Display a table of storage accounts</span></span>
```
PS C:\> Get-AzureStorageAccount | Format-Table -AutoSize -Property @{Label="Name";Expression={$_.StorageAccountName}},"Label","Location"
```

<span data-ttu-id="869bc-114">Dieser Befehl gibt ein Objekt mit allen Speicherkonten zurück, die dem aktuellen Abonnement zugeordnet sind, und gibt diese als Tabelle mit dem Kontonamen, der Kontobezeichnung und dem Speicherort aus.</span><span class="sxs-lookup"><span data-stu-id="869bc-114">This command returns an object with all the storage accounts associated with the current subscription, and outputs them as a table showing the account name, the account label, and the storage location.</span></span>

## <span data-ttu-id="869bc-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="869bc-115">PARAMETERS</span></span>

### <span data-ttu-id="869bc-116">-Information</span><span class="sxs-lookup"><span data-stu-id="869bc-116">-InformationAction</span></span>
<span data-ttu-id="869bc-117">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="869bc-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="869bc-118">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="869bc-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="869bc-119">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="869bc-119">Continue</span></span>
- <span data-ttu-id="869bc-120">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="869bc-120">Ignore</span></span>
- <span data-ttu-id="869bc-121">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="869bc-121">Inquire</span></span>
- <span data-ttu-id="869bc-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="869bc-122">SilentlyContinue</span></span>
- <span data-ttu-id="869bc-123">Beenden</span><span class="sxs-lookup"><span data-stu-id="869bc-123">Stop</span></span>
- <span data-ttu-id="869bc-124">Anhalten</span><span class="sxs-lookup"><span data-stu-id="869bc-124">Suspend</span></span>

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

### <span data-ttu-id="869bc-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="869bc-125">-InformationVariable</span></span>
<span data-ttu-id="869bc-126">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="869bc-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="869bc-127">-Profil</span><span class="sxs-lookup"><span data-stu-id="869bc-127">-Profile</span></span>
<span data-ttu-id="869bc-128">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="869bc-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="869bc-129">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="869bc-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="869bc-130">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="869bc-130">-StorageAccountName</span></span>
<span data-ttu-id="869bc-131">Gibt den Namen eines speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="869bc-131">Specifies the name of a storage account.</span></span>
<span data-ttu-id="869bc-132">Falls angegeben, gibt dieses Cmdlet nur das angegebene Speicherkonto Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="869bc-132">If specified, this cmdlet returns only the specified storage account object.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="869bc-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="869bc-133">CommonParameters</span></span>
<span data-ttu-id="869bc-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="869bc-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="869bc-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="869bc-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="869bc-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="869bc-136">INPUTS</span></span>

## <span data-ttu-id="869bc-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="869bc-137">OUTPUTS</span></span>

### <span data-ttu-id="869bc-138">ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="869bc-138">ManagementOperationContext</span></span>

## <span data-ttu-id="869bc-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="869bc-139">NOTES</span></span>
* <span data-ttu-id="869bc-140">Geben Sie `help node-dev` an, um Hilfe zu Node.js entwicklungsbezogenen Cmdlets zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="869bc-140">Type `help node-dev` to get help on Node.js development-related cmdlets.</span></span> <span data-ttu-id="869bc-141">Geben Sie `help php-dev` an, um Hilfe zu den PHP-entwicklungsbezogenen Cmdlets zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="869bc-141">Type `help php-dev` to get help on PHP development-related cmdlets.</span></span>

## <span data-ttu-id="869bc-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="869bc-142">RELATED LINKS</span></span>

[<span data-ttu-id="869bc-143">Neu – AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="869bc-143">New-AzureStorageAccount</span></span>](./New-AzureStorageAccount.md)

[<span data-ttu-id="869bc-144">Satz-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="869bc-144">Set-AzureStorageAccount</span></span>](./Set-AzureStorageAccount.md)



---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 35588231-CBAC-4411-9531-9A06BD298ACA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7fdcad4b3a0f41f0589e49d4b33a767b93267855
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005754"
---
# <span data-ttu-id="09dc0-101">Get-AzureStorageKey</span><span class="sxs-lookup"><span data-stu-id="09dc0-101">Get-AzureStorageKey</span></span>

## <span data-ttu-id="09dc0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="09dc0-102">SYNOPSIS</span></span>
<span data-ttu-id="09dc0-103">Gibt den primären und sekundären speicherkontoschlüssel für ein Azure Storage-Konto zurück.</span><span class="sxs-lookup"><span data-stu-id="09dc0-103">Returns the primary and secondary storage account keys for an Azure storage account.</span></span>

## <span data-ttu-id="09dc0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="09dc0-104">SYNTAX</span></span>

```
Get-AzureStorageKey [-StorageAccountName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="09dc0-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="09dc0-105">DESCRIPTION</span></span>
<span data-ttu-id="09dc0-106">Das Cmdlet " **Get-AzureStorageKey** " gibt ein Objekt mit dem Namen des Azure-speicherkontos, dem primär Kontoschlüssel und dem sekundären Kontoschlüssel des angegebenen Azure-speicherkontos als Eigenschaften zurück.</span><span class="sxs-lookup"><span data-stu-id="09dc0-106">The **Get-AzureStorageKey** cmdlet returns an object with the Azure Storage account name, the primary account key, and the secondary account key of the specified Azure storage account as properties.</span></span>

## <span data-ttu-id="09dc0-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="09dc0-107">EXAMPLES</span></span>

### <span data-ttu-id="09dc0-108">Beispiel 1: Abrufen eines Objekts, das primäre und sekundäre Speicherschlüssel enthält</span><span class="sxs-lookup"><span data-stu-id="09dc0-108">Example 1: Get an object that contains primary and secondary storage keys</span></span>
```
PS C:\> Get-AzureStorageKey -StorageAccountName "ContosoStore01"
```

<span data-ttu-id="09dc0-109">Dieser Befehl ruft ein Objekt mit den primären und sekundären Speicher Schlüsseln für das ContosoStore01-Speicherkonto ab.</span><span class="sxs-lookup"><span data-stu-id="09dc0-109">This command gets an object with the primary and secondary storage keys for the ContosoStore01 storage account.</span></span>

### <span data-ttu-id="09dc0-110">Beispiel 2: Abrufen des primären Speicherkonto Schlüssels und speichern in einer Variablen</span><span class="sxs-lookup"><span data-stu-id="09dc0-110">Example 2: Get the primary storage account key and store it in a variable</span></span>
```
PS C:\> $ContosoStoreKey = (Get-AzureStorageKey -StorageAccountName "ContosoStore01").Primary
```

<span data-ttu-id="09dc0-111">Mit diesem Befehl wird der primäre speicherkontoschlüssel für das ContosoStore01-Speicherkonto in der $ContosoStoreKey Variablen eingefügt.</span><span class="sxs-lookup"><span data-stu-id="09dc0-111">This command puts the primary storage account key for the ContosoStore01 storage account in the $ContosoStoreKey variable.</span></span>

## <span data-ttu-id="09dc0-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="09dc0-112">PARAMETERS</span></span>

### <span data-ttu-id="09dc0-113">-Information</span><span class="sxs-lookup"><span data-stu-id="09dc0-113">-InformationAction</span></span>
<span data-ttu-id="09dc0-114">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="09dc0-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="09dc0-115">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="09dc0-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="09dc0-116">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="09dc0-116">Continue</span></span>
- <span data-ttu-id="09dc0-117">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="09dc0-117">Ignore</span></span>
- <span data-ttu-id="09dc0-118">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="09dc0-118">Inquire</span></span>
- <span data-ttu-id="09dc0-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="09dc0-119">SilentlyContinue</span></span>
- <span data-ttu-id="09dc0-120">Beenden</span><span class="sxs-lookup"><span data-stu-id="09dc0-120">Stop</span></span>
- <span data-ttu-id="09dc0-121">Anhalten</span><span class="sxs-lookup"><span data-stu-id="09dc0-121">Suspend</span></span>

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

### <span data-ttu-id="09dc0-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="09dc0-122">-InformationVariable</span></span>
<span data-ttu-id="09dc0-123">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="09dc0-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="09dc0-124">-Profil</span><span class="sxs-lookup"><span data-stu-id="09dc0-124">-Profile</span></span>
<span data-ttu-id="09dc0-125">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="09dc0-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="09dc0-126">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="09dc0-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="09dc0-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="09dc0-127">-StorageAccountName</span></span>
<span data-ttu-id="09dc0-128">Gibt den Namen des speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="09dc0-128">Specifies the storage account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09dc0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09dc0-129">CommonParameters</span></span>
<span data-ttu-id="09dc0-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09dc0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09dc0-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09dc0-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09dc0-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="09dc0-132">INPUTS</span></span>

## <span data-ttu-id="09dc0-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="09dc0-133">OUTPUTS</span></span>

## <span data-ttu-id="09dc0-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="09dc0-134">NOTES</span></span>
* <span data-ttu-id="09dc0-135">Verwenden Sie den Befehl, um Hilfe zu Node.js zu erhalten `help node-dev` .</span><span class="sxs-lookup"><span data-stu-id="09dc0-135">To get help with Node.js, use the `help node-dev` command.</span></span> <span data-ttu-id="09dc0-136">Wenn Sie Hilfe zu PHP-Erweiterungen benötigen, verwenden Sie den `help php-dev` Befehl.</span><span class="sxs-lookup"><span data-stu-id="09dc0-136">For help with PHP extensions, use the `help php-dev` command.</span></span>

## <span data-ttu-id="09dc0-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="09dc0-137">RELATED LINKS</span></span>

[<span data-ttu-id="09dc0-138">Get-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="09dc0-138">Get-AzureStorageAccount</span></span>](./Get-AzureStorageAccount.md)

[<span data-ttu-id="09dc0-139">Neu – AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="09dc0-139">New-AzureStorageAccount</span></span>](./New-AzureStorageAccount.md)

[<span data-ttu-id="09dc0-140">Neu – AzureStorageKey</span><span class="sxs-lookup"><span data-stu-id="09dc0-140">New-AzureStorageKey</span></span>](./New-AzureStorageKey.md)

[<span data-ttu-id="09dc0-141">Remove-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="09dc0-141">Remove-AzureStorageAccount</span></span>](./Remove-AzureStorageAccount.md)

[<span data-ttu-id="09dc0-142">Satz-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="09dc0-142">Set-AzureStorageAccount</span></span>](./Set-AzureStorageAccount.md)



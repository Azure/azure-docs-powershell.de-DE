---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 09ABE9E2-1080-4DEF-92DD-B8FF4C8B308C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9afdaafa57592239d0c24870e4459d650fac84c3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006409"
---
# <span data-ttu-id="a290b-101">New-AzureStorageKey</span><span class="sxs-lookup"><span data-stu-id="a290b-101">New-AzureStorageKey</span></span>

## <span data-ttu-id="a290b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a290b-102">SYNOPSIS</span></span>
<span data-ttu-id="a290b-103">Regeneriert Speicherschlüssel für ein Azure Storage-Konto.</span><span class="sxs-lookup"><span data-stu-id="a290b-103">Regenerates storage keys for an Azure storage account.</span></span>

## <span data-ttu-id="a290b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a290b-104">SYNTAX</span></span>

```
New-AzureStorageKey [-KeyType] <String> [-StorageAccountName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="a290b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a290b-105">DESCRIPTION</span></span>
<span data-ttu-id="a290b-106">Das Cmdlet **New-AzureStorageKey** generiert den primären oder sekundären Schlüssel für ein Azure Storage-Konto erneut.</span><span class="sxs-lookup"><span data-stu-id="a290b-106">The **New-AzureStorageKey** cmdlet regenerates the primary or secondary key for an Azure Storage account.</span></span>
<span data-ttu-id="a290b-107">Sie gibt ein Objekt zurück, das den Namen des speicherkontos, den Primärschlüssel und den sekundären Schlüssel als Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="a290b-107">It returns an object that contains the storage account name, primary key, and secondary key as properties.</span></span>

## <span data-ttu-id="a290b-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a290b-108">EXAMPLES</span></span>

### <span data-ttu-id="a290b-109">Beispiel 1: Erneutes Generieren eines primären Speicher Schlüssels</span><span class="sxs-lookup"><span data-stu-id="a290b-109">Example 1: Regenerate a primary storage key</span></span>
```
PS C:\> New-AzureStorageKey -KeyType "Primary" -StorageAccountName "ContosoStore01"
```

<span data-ttu-id="a290b-110">Mit diesem Befehl wird der primäre Speicherschlüssel für das ContosoStore01-Speicherkonto neu generiert.</span><span class="sxs-lookup"><span data-stu-id="a290b-110">This command regenerates the primary storage key for the ContosoStore01 storage account.</span></span>

### <span data-ttu-id="a290b-111">Beispiel 2: Erneutes Generieren eines sekundären Speicher Schlüssels und speichern in einer Variablen</span><span class="sxs-lookup"><span data-stu-id="a290b-111">Example 2: Regenerate a secondary storage key and save it in a variable</span></span>
```
PS C:\> $ContosoStoreKey = New-AzureStorageKey -KeyType "Secondary" -StorageAccountName "ContosoStore01"
```

<span data-ttu-id="a290b-112">Mit diesem Befehl wird der sekundäre Speicherschlüssel für das ContosoStore01-Speicherkonto neu generiert, und die aktualisierten speicherkontoschlüssel Informationen werden im $ContosoStoreKey gespeichert.</span><span class="sxs-lookup"><span data-stu-id="a290b-112">This command regenerate the secondary storage key for the ContosoStore01 storage account and stores the updated storage account key information in the $ContosoStoreKey.</span></span>

## <span data-ttu-id="a290b-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="a290b-113">PARAMETERS</span></span>

### <span data-ttu-id="a290b-114">-Information</span><span class="sxs-lookup"><span data-stu-id="a290b-114">-InformationAction</span></span>
<span data-ttu-id="a290b-115">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="a290b-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="a290b-116">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="a290b-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a290b-117">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="a290b-117">Continue</span></span>
- <span data-ttu-id="a290b-118">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="a290b-118">Ignore</span></span>
- <span data-ttu-id="a290b-119">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="a290b-119">Inquire</span></span>
- <span data-ttu-id="a290b-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="a290b-120">SilentlyContinue</span></span>
- <span data-ttu-id="a290b-121">Beenden</span><span class="sxs-lookup"><span data-stu-id="a290b-121">Stop</span></span>
- <span data-ttu-id="a290b-122">Anhalten</span><span class="sxs-lookup"><span data-stu-id="a290b-122">Suspend</span></span>

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

### <span data-ttu-id="a290b-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="a290b-123">-InformationVariable</span></span>
<span data-ttu-id="a290b-124">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="a290b-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="a290b-125">-KeyType</span><span class="sxs-lookup"><span data-stu-id="a290b-125">-KeyType</span></span>
<span data-ttu-id="a290b-126">Gibt an, welche Taste neu generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="a290b-126">Specifies which key to regenerate.</span></span>
<span data-ttu-id="a290b-127">Gültige Werte sind: Primär und sekundär.</span><span class="sxs-lookup"><span data-stu-id="a290b-127">Valid values are: Primary and Secondary.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a290b-128">-Profil</span><span class="sxs-lookup"><span data-stu-id="a290b-128">-Profile</span></span>
<span data-ttu-id="a290b-129">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="a290b-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a290b-130">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="a290b-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a290b-131">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="a290b-131">-StorageAccountName</span></span>
<span data-ttu-id="a290b-132">Gibt den Namen des Azure-speicherkontos an, für das ein Schlüssel neu generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="a290b-132">Specifies the name of the Azure Storage account for which to regenerate a key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a290b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a290b-133">CommonParameters</span></span>
<span data-ttu-id="a290b-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a290b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a290b-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a290b-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a290b-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a290b-136">INPUTS</span></span>

## <span data-ttu-id="a290b-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a290b-137">OUTPUTS</span></span>

### <span data-ttu-id="a290b-138">StorageServiceKeys</span><span class="sxs-lookup"><span data-stu-id="a290b-138">StorageServiceKeys</span></span>

## <span data-ttu-id="a290b-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="a290b-139">NOTES</span></span>

## <span data-ttu-id="a290b-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a290b-140">RELATED LINKS</span></span>

[<span data-ttu-id="a290b-141">Get-AzureStorageKey</span><span class="sxs-lookup"><span data-stu-id="a290b-141">Get-AzureStorageKey</span></span>](./Get-AzureStorageKey.md)



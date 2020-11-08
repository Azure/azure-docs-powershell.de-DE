---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 679452A6-A6CA-4DC8-8E00-09E369505319
online version: ''
schema: 2.0.0
ms.openlocfilehash: 933c6de8e7baa55b2093a7ffc4ac28fede13bb5b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006664"
---
# <span data-ttu-id="0a440-101">Remove-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0a440-101">Remove-AzureStorageAccount</span></span>

## <span data-ttu-id="0a440-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0a440-102">SYNOPSIS</span></span>
<span data-ttu-id="0a440-103">Löscht das angegebene Speicherkonto aus einem Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0a440-103">Deletes the specified storage account from a subscription.</span></span>

## <span data-ttu-id="0a440-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0a440-104">SYNTAX</span></span>

```
Remove-AzureStorageAccount [-StorageAccountName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="0a440-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0a440-105">DESCRIPTION</span></span>
<span data-ttu-id="0a440-106">Das Cmdlet **Remove-AzureStorageAccount** entfernt ein Konto aus einem Azure-Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0a440-106">The **Remove-AzureStorageAccount** cmdlet removes an account from an Azure subscription.</span></span>

## <span data-ttu-id="0a440-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0a440-107">EXAMPLES</span></span>

### <span data-ttu-id="0a440-108">Beispiel 1: Entfernen eines speicherkontos</span><span class="sxs-lookup"><span data-stu-id="0a440-108">Example 1: Remove a storage account</span></span>
```
PS C:\> Remove-AzureStorageAccount -StorageAccountName "ContosoStore01"
```

<span data-ttu-id="0a440-109">Dieser Befehl entfernt das ContosoStore01-Speicherkonto aus dem angegebenen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0a440-109">This command removes the ContosoStore01 storage account from the specified subscription.</span></span>

## <span data-ttu-id="0a440-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="0a440-110">PARAMETERS</span></span>

### <span data-ttu-id="0a440-111">-Information</span><span class="sxs-lookup"><span data-stu-id="0a440-111">-InformationAction</span></span>
<span data-ttu-id="0a440-112">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="0a440-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="0a440-113">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="0a440-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0a440-114">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="0a440-114">Continue</span></span>
- <span data-ttu-id="0a440-115">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="0a440-115">Ignore</span></span>
- <span data-ttu-id="0a440-116">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="0a440-116">Inquire</span></span>
- <span data-ttu-id="0a440-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="0a440-117">SilentlyContinue</span></span>
- <span data-ttu-id="0a440-118">Beenden</span><span class="sxs-lookup"><span data-stu-id="0a440-118">Stop</span></span>
- <span data-ttu-id="0a440-119">Anhalten</span><span class="sxs-lookup"><span data-stu-id="0a440-119">Suspend</span></span>

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

### <span data-ttu-id="0a440-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="0a440-120">-InformationVariable</span></span>
<span data-ttu-id="0a440-121">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="0a440-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="0a440-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="0a440-122">-Profile</span></span>
<span data-ttu-id="0a440-123">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="0a440-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0a440-124">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="0a440-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0a440-125">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="0a440-125">-StorageAccountName</span></span>
<span data-ttu-id="0a440-126">Gibt den Namen des zu entfernenden speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="0a440-126">Specifies the name of the storage account to remove.</span></span>

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

### <span data-ttu-id="0a440-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a440-127">CommonParameters</span></span>
<span data-ttu-id="0a440-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a440-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a440-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a440-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a440-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0a440-130">INPUTS</span></span>

## <span data-ttu-id="0a440-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0a440-131">OUTPUTS</span></span>

## <span data-ttu-id="0a440-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="0a440-132">NOTES</span></span>

## <span data-ttu-id="0a440-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0a440-133">RELATED LINKS</span></span>

[<span data-ttu-id="0a440-134">Get-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0a440-134">Get-AzureStorageAccount</span></span>](./Get-AzureStorageAccount.md)

[<span data-ttu-id="0a440-135">Neu – AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0a440-135">New-AzureStorageAccount</span></span>](./New-AzureStorageAccount.md)

[<span data-ttu-id="0a440-136">Satz-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0a440-136">Set-AzureStorageAccount</span></span>](./Set-AzureStorageAccount.md)



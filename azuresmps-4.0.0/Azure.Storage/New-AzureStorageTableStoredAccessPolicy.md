---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: CF3B6E3B-3FC1-4871-AFE0-366B17A9E4F8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 54b28caaf39bd3d4750e341da4f4564d60b59138
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93474674"
---
# <span data-ttu-id="75c60-101">New-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="75c60-101">New-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="75c60-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="75c60-102">SYNOPSIS</span></span>
<span data-ttu-id="75c60-103">Erstellt eine gespeicherte Zugriffsrichtlinie für eine Azure-Speichertabelle.</span><span class="sxs-lookup"><span data-stu-id="75c60-103">Creates a stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="75c60-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="75c60-104">SYNTAX</span></span>

```
New-AzureStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="75c60-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="75c60-105">DESCRIPTION</span></span>
<span data-ttu-id="75c60-106">Das Cmdlet **New-AzureStorageTableStoredAccessPolicy** erstellt eine gespeicherte Zugriffsrichtlinie für eine Azure-Speichertabelle.</span><span class="sxs-lookup"><span data-stu-id="75c60-106">The **New-AzureStorageTableStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="75c60-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="75c60-107">EXAMPLES</span></span>

### <span data-ttu-id="75c60-108">Beispiel 1: Erstellen einer gespeicherten Zugriffsrichtlinie in einer Tabelle</span><span class="sxs-lookup"><span data-stu-id="75c60-108">Example 1: Create a stored access policy in a table</span></span>
```
PS C:\>New-AzureStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy02"
```

<span data-ttu-id="75c60-109">Dieser Befehl erstellt eine Access-Richtlinie mit dem Namen Policy02 in der Speichertabelle mit dem Namen myTable.</span><span class="sxs-lookup"><span data-stu-id="75c60-109">This command creates an access policy named Policy02 in the storage table named MyTable.</span></span>

## <span data-ttu-id="75c60-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="75c60-110">PARAMETERS</span></span>

### <span data-ttu-id="75c60-111">-Context</span><span class="sxs-lookup"><span data-stu-id="75c60-111">-Context</span></span>
<span data-ttu-id="75c60-112">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="75c60-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="75c60-113">Verwenden Sie das New-AzureStorageContext-Cmdlet, um einen Speicherkontext zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="75c60-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="75c60-114">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="75c60-114">-ExpiryTime</span></span>
<span data-ttu-id="75c60-115">Gibt den Zeitpunkt an, zu dem die gespeicherte Zugriffsrichtlinie ungültig wird.</span><span class="sxs-lookup"><span data-stu-id="75c60-115">Specifies the time at which the stored access policy becomes invalid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75c60-116">-Berechtigung</span><span class="sxs-lookup"><span data-stu-id="75c60-116">-Permission</span></span>
<span data-ttu-id="75c60-117">Gibt die Ebene des öffentlichen Zugriffs auf diese Speichertabelle an.</span><span class="sxs-lookup"><span data-stu-id="75c60-117">Specifies the level of public access to this storage table.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75c60-118">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="75c60-118">-Policy</span></span>
<span data-ttu-id="75c60-119">Gibt eine Richtlinie für den gespeicherten Zugriff an, die die Berechtigungen für dieses SAS-Token (Shared Access Signature) enthält.</span><span class="sxs-lookup"><span data-stu-id="75c60-119">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75c60-120">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="75c60-120">-StartTime</span></span>
<span data-ttu-id="75c60-121">Gibt den Zeitpunkt an, zu dem die gespeicherte Zugriffsrichtlinie gültig wird.</span><span class="sxs-lookup"><span data-stu-id="75c60-121">Specifies the time at which the stored access policy becomes valid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75c60-122">-Tabelle</span><span class="sxs-lookup"><span data-stu-id="75c60-122">-Table</span></span>
<span data-ttu-id="75c60-123">Gibt den Namen der Azure-Speichertabelle an.</span><span class="sxs-lookup"><span data-stu-id="75c60-123">Specifies the Azure storage table name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="75c60-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75c60-124">CommonParameters</span></span>
<span data-ttu-id="75c60-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75c60-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75c60-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75c60-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75c60-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="75c60-127">INPUTS</span></span>

## <span data-ttu-id="75c60-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="75c60-128">OUTPUTS</span></span>

## <span data-ttu-id="75c60-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="75c60-129">NOTES</span></span>

## <span data-ttu-id="75c60-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="75c60-130">RELATED LINKS</span></span>

[<span data-ttu-id="75c60-131">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="75c60-131">Get-AzureStorageTableStoredAccessPolicy</span></span>](./Get-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="75c60-132">Neu – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="75c60-132">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="75c60-133">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="75c60-133">Remove-AzureStorageTableStoredAccessPolicy</span></span>](./Remove-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="75c60-134">Satz-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="75c60-134">Set-AzureStorageTableStoredAccessPolicy</span></span>](./Set-AzureStorageTableStoredAccessPolicy.md)



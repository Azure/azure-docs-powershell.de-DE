---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 351145AC-7C1E-4EB7-A17D-B8B7D8ED8DAB
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/New-AzStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/New-AzStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: cda91974a8498e26f57d3a30381fe97791b2d354
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842983"
---
# <span data-ttu-id="56454-101">New-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="56454-101">New-AzStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="56454-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="56454-102">SYNOPSIS</span></span>
<span data-ttu-id="56454-103">Erstellt eine gespeicherte Zugriffsrichtlinie für eine Azure Storage-Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="56454-103">Creates a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="56454-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="56454-104">SYNTAX</span></span>

```
New-AzStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="56454-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="56454-105">DESCRIPTION</span></span>
<span data-ttu-id="56454-106">Das Cmdlet **New-AzStorageQueueStoredAccessPolicy** erstellt eine gespeicherte Zugriffsrichtlinie für eine Azure Storage-Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="56454-106">The **New-AzStorageQueueStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="56454-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="56454-107">EXAMPLES</span></span>

### <span data-ttu-id="56454-108">Beispiel 1: Erstellen einer gespeicherten Zugriffsrichtlinie in einer Speicherwarteschlange</span><span class="sxs-lookup"><span data-stu-id="56454-108">Example 1: Create a stored access policy in a storage queue</span></span>
```
PS C:\>New-AzStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy01"
```

<span data-ttu-id="56454-109">Dieser Befehl erstellt eine Access-Richtlinie mit dem Namen Policy01 in der Speicherwarteschlange mit dem Namen myQueue.</span><span class="sxs-lookup"><span data-stu-id="56454-109">This command creates an access policy named Policy01 in the storage queue named MyQueue.</span></span>

## <span data-ttu-id="56454-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="56454-110">PARAMETERS</span></span>

### <span data-ttu-id="56454-111">-Context</span><span class="sxs-lookup"><span data-stu-id="56454-111">-Context</span></span>
<span data-ttu-id="56454-112">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="56454-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="56454-113">Verwenden Sie das New-AzStorageContext-Cmdlet, um einen Speicherkontext zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="56454-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="56454-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56454-114">-DefaultProfile</span></span>
<span data-ttu-id="56454-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="56454-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56454-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="56454-116">-ExpiryTime</span></span>
<span data-ttu-id="56454-117">Gibt den Zeitpunkt an, zu dem die gespeicherte Zugriffsrichtlinie ungültig wird.</span><span class="sxs-lookup"><span data-stu-id="56454-117">Specifies the time at which the stored access policy becomes invalid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56454-118">-Berechtigung</span><span class="sxs-lookup"><span data-stu-id="56454-118">-Permission</span></span>
<span data-ttu-id="56454-119">Gibt Berechtigungen in der gespeicherten Zugriffsrichtlinie an, um auf die Speicherwarteschlange zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="56454-119">Specifies permissions in the stored access policy to access the storage queue.</span></span>
<span data-ttu-id="56454-120">Beachten Sie, dass es sich um eine Zeichenfolge wie `rwd` (für lesen, schreiben und löschen) handelt.</span><span class="sxs-lookup"><span data-stu-id="56454-120">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56454-121">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="56454-121">-Policy</span></span>
<span data-ttu-id="56454-122">Gibt einen Namen für die gespeicherte Zugriffsrichtlinie an.</span><span class="sxs-lookup"><span data-stu-id="56454-122">Specifies a name for the stored access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56454-123">-Queue</span><span class="sxs-lookup"><span data-stu-id="56454-123">-Queue</span></span>
<span data-ttu-id="56454-124">Gibt den Namen der Azure-Speicherwarteschlange an.</span><span class="sxs-lookup"><span data-stu-id="56454-124">Specifies the Azure storage queue name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="56454-125">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="56454-125">-StartTime</span></span>
<span data-ttu-id="56454-126">Gibt den Zeitpunkt an, zu dem die gespeicherte Zugriffsrichtlinie gültig wird.</span><span class="sxs-lookup"><span data-stu-id="56454-126">Specifies the time at which the stored access policy becomes valid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56454-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56454-127">CommonParameters</span></span>
<span data-ttu-id="56454-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56454-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56454-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56454-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56454-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="56454-130">INPUTS</span></span>

### <span data-ttu-id="56454-131">System. String</span><span class="sxs-lookup"><span data-stu-id="56454-131">System.String</span></span>

### <span data-ttu-id="56454-132">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="56454-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="56454-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="56454-133">OUTPUTS</span></span>

### <span data-ttu-id="56454-134">System. String</span><span class="sxs-lookup"><span data-stu-id="56454-134">System.String</span></span>

## <span data-ttu-id="56454-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="56454-135">NOTES</span></span>

## <span data-ttu-id="56454-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="56454-136">RELATED LINKS</span></span>

[<span data-ttu-id="56454-137">Get-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="56454-137">Get-AzStorageQueueStoredAccessPolicy</span></span>](./Get-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="56454-138">Neu – AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="56454-138">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="56454-139">Remove-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="56454-139">Remove-AzStorageQueueStoredAccessPolicy</span></span>](./Remove-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="56454-140">Satz-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="56454-140">Set-AzStorageQueueStoredAccessPolicy</span></span>](./Set-AzStorageQueueStoredAccessPolicy.md)



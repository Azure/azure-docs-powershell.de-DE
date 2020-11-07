---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 351145AC-7C1E-4EB7-A17D-B8B7D8ED8DAB
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragequeuestoredaccesspolicy
schema: 2.0.0
ms.openlocfilehash: 054a5d979a13f5592f062f729e4c8c393a35134a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849811"
---
# <span data-ttu-id="51c91-101">New-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="51c91-101">New-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="51c91-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="51c91-102">SYNOPSIS</span></span>
<span data-ttu-id="51c91-103">Erstellt eine gespeicherte Zugriffsrichtlinie für eine Azure Storage-Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="51c91-103">Creates a stored access policy for an Azure storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="51c91-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="51c91-104">SYNTAX</span></span>

```
New-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="51c91-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="51c91-105">DESCRIPTION</span></span>
<span data-ttu-id="51c91-106">Das Cmdlet **New-AzureStorageQueueStoredAccessPolicy** erstellt eine gespeicherte Zugriffsrichtlinie für eine Azure Storage-Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="51c91-106">The **New-AzureStorageQueueStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="51c91-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="51c91-107">EXAMPLES</span></span>

### <span data-ttu-id="51c91-108">Beispiel 1: Erstellen einer gespeicherten Zugriffsrichtlinie in einer Speicherwarteschlange</span><span class="sxs-lookup"><span data-stu-id="51c91-108">Example 1: Create a stored access policy in a storage queue</span></span>
```
PS C:\>New-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy01"
```

<span data-ttu-id="51c91-109">Dieser Befehl erstellt eine Access-Richtlinie mit dem Namen Policy01 in der Speicherwarteschlange mit dem Namen myQueue.</span><span class="sxs-lookup"><span data-stu-id="51c91-109">This command creates an access policy named Policy01 in the storage queue named MyQueue.</span></span>

## <span data-ttu-id="51c91-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="51c91-110">PARAMETERS</span></span>

### <span data-ttu-id="51c91-111">-Context</span><span class="sxs-lookup"><span data-stu-id="51c91-111">-Context</span></span>
<span data-ttu-id="51c91-112">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="51c91-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="51c91-113">Verwenden Sie das New-AzureStorageContext-Cmdlet, um einen Speicherkontext zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="51c91-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="51c91-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51c91-114">-DefaultProfile</span></span>
<span data-ttu-id="51c91-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="51c91-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51c91-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="51c91-116">-ExpiryTime</span></span>
<span data-ttu-id="51c91-117">Gibt den Zeitpunkt an, zu dem die gespeicherte Zugriffsrichtlinie ungültig wird.</span><span class="sxs-lookup"><span data-stu-id="51c91-117">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="51c91-118">-Berechtigung</span><span class="sxs-lookup"><span data-stu-id="51c91-118">-Permission</span></span>
<span data-ttu-id="51c91-119">Gibt Berechtigungen in der gespeicherten Zugriffsrichtlinie an, um auf die Speicherwarteschlange zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="51c91-119">Specifies permissions in the stored access policy to access the storage queue.</span></span>
<span data-ttu-id="51c91-120">Beachten Sie, dass es sich um eine Zeichenfolge wie `rwd` (für lesen, schreiben und löschen) handelt.</span><span class="sxs-lookup"><span data-stu-id="51c91-120">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="51c91-121">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="51c91-121">-Policy</span></span>
<span data-ttu-id="51c91-122">Gibt einen Namen für die gespeicherte Zugriffsrichtlinie an.</span><span class="sxs-lookup"><span data-stu-id="51c91-122">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="51c91-123">-Queue</span><span class="sxs-lookup"><span data-stu-id="51c91-123">-Queue</span></span>
<span data-ttu-id="51c91-124">Gibt den Namen der Azure-Speicherwarteschlange an.</span><span class="sxs-lookup"><span data-stu-id="51c91-124">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="51c91-125">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="51c91-125">-StartTime</span></span>
<span data-ttu-id="51c91-126">Gibt den Zeitpunkt an, zu dem die gespeicherte Zugriffsrichtlinie gültig wird.</span><span class="sxs-lookup"><span data-stu-id="51c91-126">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="51c91-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51c91-127">CommonParameters</span></span>
<span data-ttu-id="51c91-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51c91-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51c91-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51c91-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51c91-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="51c91-130">INPUTS</span></span>

### <span data-ttu-id="51c91-131">System. String</span><span class="sxs-lookup"><span data-stu-id="51c91-131">System.String</span></span>

### <span data-ttu-id="51c91-132">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="51c91-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="51c91-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="51c91-133">OUTPUTS</span></span>

### <span data-ttu-id="51c91-134">System. String</span><span class="sxs-lookup"><span data-stu-id="51c91-134">System.String</span></span>

## <span data-ttu-id="51c91-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="51c91-135">NOTES</span></span>

## <span data-ttu-id="51c91-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="51c91-136">RELATED LINKS</span></span>

[<span data-ttu-id="51c91-137">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="51c91-137">Get-AzureStorageQueueStoredAccessPolicy</span></span>](./Get-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="51c91-138">Neu – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="51c91-138">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="51c91-139">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="51c91-139">Remove-AzureStorageQueueStoredAccessPolicy</span></span>](./Remove-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="51c91-140">Satz-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="51c91-140">Set-AzureStorageQueueStoredAccessPolicy</span></span>](./Set-AzureStorageQueueStoredAccessPolicy.md)



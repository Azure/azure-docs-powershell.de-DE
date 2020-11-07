---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: F1EC601C-3ADD-402A-A5F7-84A95D312187
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: 9c61542aeb79cdcaa90d4ac32be4be38649e4abd
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843067"
---
# <span data-ttu-id="0e677-101">Get-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="0e677-101">Get-AzStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="0e677-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0e677-102">SYNOPSIS</span></span>
<span data-ttu-id="0e677-103">Ruft die gespeicherte Zugriffsrichtlinie oder Richtlinien für eine Azure Storage-Warteschlange ab.</span><span class="sxs-lookup"><span data-stu-id="0e677-103">Gets the stored access policy or policies for an Azure storage queue.</span></span>

## <span data-ttu-id="0e677-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0e677-104">SYNTAX</span></span>

```
Get-AzStorageQueueStoredAccessPolicy [-Queue] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e677-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0e677-105">DESCRIPTION</span></span>
<span data-ttu-id="0e677-106">Das Cmdlet " **Get-AzStorageQueueStoredAccessPolicy** " listet die gespeicherten Zugriffsrichtlinien oder Richtlinien für eine Azure-Speicherwarteschlange auf.</span><span class="sxs-lookup"><span data-stu-id="0e677-106">The **Get-AzStorageQueueStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage queue.</span></span>

## <span data-ttu-id="0e677-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0e677-107">EXAMPLES</span></span>

### <span data-ttu-id="0e677-108">Beispiel 1: Abrufen einer gespeicherten Zugriffsrichtlinie in der Warteschlange</span><span class="sxs-lookup"><span data-stu-id="0e677-108">Example 1: Get a stored access policy in the queue</span></span>
```
PS C:\>Get-AzStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy12"
```

<span data-ttu-id="0e677-109">Dieser Befehl ruft die Access-Richtlinie mit dem Namen Policy12 in der Speicherwarteschlange mit dem Namen myQueue ab.</span><span class="sxs-lookup"><span data-stu-id="0e677-109">This command gets the access policy named Policy12 in the storage queue named MyQueue.</span></span>

### <span data-ttu-id="0e677-110">Beispiel 2: Abrufen aller gespeicherten Zugriffsrichtlinien in der Warteschlange</span><span class="sxs-lookup"><span data-stu-id="0e677-110">Example 2: Get all stored access policies in the queue</span></span>
```
PS C:\>Get-AzStorageQueueStoredAccessPolicy -Queue "MyQueue"
```

<span data-ttu-id="0e677-111">Dieser Befehl ruft alle gespeicherten Zugriffsrichtlinien in der Warteschlange mit dem Namen myQueue ab.</span><span class="sxs-lookup"><span data-stu-id="0e677-111">This command gets all stored access policies in the queue named MyQueue.</span></span>

## <span data-ttu-id="0e677-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="0e677-112">PARAMETERS</span></span>

### <span data-ttu-id="0e677-113">-Context</span><span class="sxs-lookup"><span data-stu-id="0e677-113">-Context</span></span>
<span data-ttu-id="0e677-114">Gibt den Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="0e677-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="0e677-115">Verwenden Sie das New-AzStorageContext-Cmdlet, um einen Speicherkontext zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="0e677-115">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="0e677-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e677-116">-DefaultProfile</span></span>
<span data-ttu-id="0e677-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0e677-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e677-118">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="0e677-118">-Policy</span></span>
<span data-ttu-id="0e677-119">Gibt eine Richtlinie für den gespeicherten Zugriff an, die die Berechtigungen für dieses SAS-Token (Shared Access Signature) enthält.</span><span class="sxs-lookup"><span data-stu-id="0e677-119">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e677-120">-Queue</span><span class="sxs-lookup"><span data-stu-id="0e677-120">-Queue</span></span>
<span data-ttu-id="0e677-121">Gibt den Namen der Azure-Speicherwarteschlange an.</span><span class="sxs-lookup"><span data-stu-id="0e677-121">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="0e677-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e677-122">CommonParameters</span></span>
<span data-ttu-id="0e677-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e677-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e677-124">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e677-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e677-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0e677-125">INPUTS</span></span>

### <span data-ttu-id="0e677-126">System. String</span><span class="sxs-lookup"><span data-stu-id="0e677-126">System.String</span></span>

### <span data-ttu-id="0e677-127">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="0e677-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="0e677-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0e677-128">OUTPUTS</span></span>

### <span data-ttu-id="0e677-129">Microsoft. WindowsAz. Storage. Queue. SharedAccessQueuePolicy</span><span class="sxs-lookup"><span data-stu-id="0e677-129">Microsoft.WindowsAz.Storage.Queue.SharedAccessQueuePolicy</span></span>

## <span data-ttu-id="0e677-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="0e677-130">NOTES</span></span>

## <span data-ttu-id="0e677-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0e677-131">RELATED LINKS</span></span>

[<span data-ttu-id="0e677-132">Neu – AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="0e677-132">New-AzStorageQueueStoredAccessPolicy</span></span>](./New-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="0e677-133">Remove-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="0e677-133">Remove-AzStorageQueueStoredAccessPolicy</span></span>](./Remove-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="0e677-134">Satz-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="0e677-134">Set-AzStorageQueueStoredAccessPolicy</span></span>](./Set-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="0e677-135">Neu – AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="0e677-135">New-AzStorageContext</span></span>](./New-AzStorageContext.md)



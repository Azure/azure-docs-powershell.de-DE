---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: BF5526C1-11B9-47A8-A5A6-CB275B470A9E
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragetablestoredaccesspolicy
schema: 2.0.0
ms.openlocfilehash: a9c141684eb924ed0b969c469214d92b847e13db
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849843"
---
# <span data-ttu-id="a963a-101">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a963a-101">Get-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="a963a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a963a-102">SYNOPSIS</span></span>
<span data-ttu-id="a963a-103">Ruft die gespeicherte Zugriffsrichtlinie oder Richtlinien für eine Azure-Speichertabelle ab.</span><span class="sxs-lookup"><span data-stu-id="a963a-103">Gets the stored access policy or policies for an Azure storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a963a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a963a-104">SYNTAX</span></span>

```
Get-AzureStorageTableStoredAccessPolicy [-Table] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a963a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a963a-105">DESCRIPTION</span></span>
<span data-ttu-id="a963a-106">Das Cmdlet " **Get-AzureStorageTableStoredAccessPolicy** " listet die gespeicherte Zugriffsrichtlinie oder Richtlinien für eine Azure-Speichertabelle auf.</span><span class="sxs-lookup"><span data-stu-id="a963a-106">The **Get-AzureStorageTableStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage table.</span></span>

## <span data-ttu-id="a963a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a963a-107">EXAMPLES</span></span>

### <span data-ttu-id="a963a-108">Beispiel 1: Abrufen einer gespeicherten Zugriffsrichtlinie in einer Speichertabelle</span><span class="sxs-lookup"><span data-stu-id="a963a-108">Example 1: Get a stored access policy in a storage table</span></span>
```
PS C:\>Get-AzureStorageTableStoredAccessPolicy -Table "Table02" -Policy "Policy50"
```

<span data-ttu-id="a963a-109">Dieser Befehl ruft die Access-Richtlinie mit dem Namen Policy50 in der Speichertabelle mit dem Namen Table02 ab.</span><span class="sxs-lookup"><span data-stu-id="a963a-109">This command gets the access policy named Policy50 in the storage table named Table02.</span></span>

### <span data-ttu-id="a963a-110">Beispiel 2: Abrufen aller gespeicherten Zugriffsrichtlinien in einer Speichertabelle</span><span class="sxs-lookup"><span data-stu-id="a963a-110">Example 2: Get all stored access policies in a storage table</span></span>
```
PS C:\>Get-AzureStorageTableStoredAccessPolicy -Table "Table02"
```

<span data-ttu-id="a963a-111">Dieser Befehl ruft alle Zugriffsrichtlinien in der Tabelle mit dem Namen Table02 ab.</span><span class="sxs-lookup"><span data-stu-id="a963a-111">This command gets all access policies in the table named Table02.</span></span>

## <span data-ttu-id="a963a-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="a963a-112">PARAMETERS</span></span>

### <span data-ttu-id="a963a-113">-Context</span><span class="sxs-lookup"><span data-stu-id="a963a-113">-Context</span></span>
<span data-ttu-id="a963a-114">Gibt den Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="a963a-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="a963a-115">Verwenden Sie das New-AzureStorageContext-Cmdlet, um einen Speicherkontext zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="a963a-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="a963a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a963a-116">-DefaultProfile</span></span>
<span data-ttu-id="a963a-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a963a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a963a-118">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="a963a-118">-Policy</span></span>
<span data-ttu-id="a963a-119">Gibt eine Richtlinie für den gespeicherten Zugriff an, die die Berechtigungen für dieses SAS-Token (Shared Access Signature) enthält.</span><span class="sxs-lookup"><span data-stu-id="a963a-119">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

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

### <span data-ttu-id="a963a-120">-Tabelle</span><span class="sxs-lookup"><span data-stu-id="a963a-120">-Table</span></span>
<span data-ttu-id="a963a-121">Gibt den Namen der Azure-Speichertabelle an.</span><span class="sxs-lookup"><span data-stu-id="a963a-121">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="a963a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a963a-122">CommonParameters</span></span>
<span data-ttu-id="a963a-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a963a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a963a-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a963a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a963a-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a963a-125">INPUTS</span></span>

### <span data-ttu-id="a963a-126">System. String</span><span class="sxs-lookup"><span data-stu-id="a963a-126">System.String</span></span>

### <span data-ttu-id="a963a-127">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="a963a-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="a963a-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a963a-128">OUTPUTS</span></span>

### <span data-ttu-id="a963a-129">Microsoft. WindowsAzure. Storage. Table. SharedAccessTablePolicy</span><span class="sxs-lookup"><span data-stu-id="a963a-129">Microsoft.WindowsAzure.Storage.Table.SharedAccessTablePolicy</span></span>

## <span data-ttu-id="a963a-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="a963a-130">NOTES</span></span>

## <span data-ttu-id="a963a-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a963a-131">RELATED LINKS</span></span>

[<span data-ttu-id="a963a-132">Neu – AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a963a-132">New-AzureStorageTableStoredAccessPolicy</span></span>](./New-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="a963a-133">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a963a-133">Remove-AzureStorageTableStoredAccessPolicy</span></span>](./Remove-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="a963a-134">Satz-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a963a-134">Set-AzureStorageTableStoredAccessPolicy</span></span>](./Set-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="a963a-135">Neu – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="a963a-135">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)



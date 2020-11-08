---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BF5526C1-11B9-47A8-A5A6-CB275B470A9E
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTableStoredAccessPolicy.md
ms.openlocfilehash: b17a294392ca4336d4a96e5d136ad4e321eb45a7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94010380"
---
# <span data-ttu-id="b4fc4-101">Get-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b4fc4-101">Get-AzStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="b4fc4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b4fc4-102">SYNOPSIS</span></span>
<span data-ttu-id="b4fc4-103">Ruft die gespeicherte Zugriffsrichtlinie oder Richtlinien für eine Azure-Speichertabelle ab.</span><span class="sxs-lookup"><span data-stu-id="b4fc4-103">Gets the stored access policy or policies for an Azure storage table.</span></span>

## <span data-ttu-id="b4fc4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b4fc4-104">SYNTAX</span></span>

```
Get-AzStorageTableStoredAccessPolicy [-Table] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4fc4-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b4fc4-105">DESCRIPTION</span></span>
<span data-ttu-id="b4fc4-106">Das Cmdlet " **Get-AzStorageTableStoredAccessPolicy** " listet die gespeicherte Zugriffsrichtlinie oder Richtlinien für eine Azure-Speichertabelle auf.</span><span class="sxs-lookup"><span data-stu-id="b4fc4-106">The **Get-AzStorageTableStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage table.</span></span>

## <span data-ttu-id="b4fc4-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b4fc4-107">EXAMPLES</span></span>

### <span data-ttu-id="b4fc4-108">Beispiel 1: Abrufen einer gespeicherten Zugriffsrichtlinie in einer Speichertabelle</span><span class="sxs-lookup"><span data-stu-id="b4fc4-108">Example 1: Get a stored access policy in a storage table</span></span>
```
PS C:\>Get-AzStorageTableStoredAccessPolicy -Table "Table02" -Policy "Policy50"
```

<span data-ttu-id="b4fc4-109">Dieser Befehl ruft die Access-Richtlinie mit dem Namen Policy50 in der Speichertabelle mit dem Namen Table02 ab.</span><span class="sxs-lookup"><span data-stu-id="b4fc4-109">This command gets the access policy named Policy50 in the storage table named Table02.</span></span>

### <span data-ttu-id="b4fc4-110">Beispiel 2: Abrufen aller gespeicherten Zugriffsrichtlinien in einer Speichertabelle</span><span class="sxs-lookup"><span data-stu-id="b4fc4-110">Example 2: Get all stored access policies in a storage table</span></span>
```
PS C:\>Get-AzStorageTableStoredAccessPolicy -Table "Table02"
```

<span data-ttu-id="b4fc4-111">Dieser Befehl ruft alle Zugriffsrichtlinien in der Tabelle mit dem Namen Table02 ab.</span><span class="sxs-lookup"><span data-stu-id="b4fc4-111">This command gets all access policies in the table named Table02.</span></span>

## <span data-ttu-id="b4fc4-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="b4fc4-112">PARAMETERS</span></span>

### <span data-ttu-id="b4fc4-113">-Context</span><span class="sxs-lookup"><span data-stu-id="b4fc4-113">-Context</span></span>
<span data-ttu-id="b4fc4-114">Gibt den Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="b4fc4-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="b4fc4-115">Verwenden Sie das New-AzStorageContext-Cmdlet, um einen Speicherkontext zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="b4fc4-115">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="b4fc4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4fc4-116">-DefaultProfile</span></span>
<span data-ttu-id="b4fc4-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b4fc4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4fc4-118">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="b4fc4-118">-Policy</span></span>
<span data-ttu-id="b4fc4-119">Gibt eine Richtlinie für den gespeicherten Zugriff an, die die Berechtigungen für dieses SAS-Token (Shared Access Signature) enthält.</span><span class="sxs-lookup"><span data-stu-id="b4fc4-119">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

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

### <span data-ttu-id="b4fc4-120">-Tabelle</span><span class="sxs-lookup"><span data-stu-id="b4fc4-120">-Table</span></span>
<span data-ttu-id="b4fc4-121">Gibt den Namen der Azure-Speichertabelle an.</span><span class="sxs-lookup"><span data-stu-id="b4fc4-121">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="b4fc4-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4fc4-122">CommonParameters</span></span>
<span data-ttu-id="b4fc4-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4fc4-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4fc4-124">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4fc4-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4fc4-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b4fc4-125">INPUTS</span></span>

### <span data-ttu-id="b4fc4-126">System. String</span><span class="sxs-lookup"><span data-stu-id="b4fc4-126">System.String</span></span>

### <span data-ttu-id="b4fc4-127">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="b4fc4-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="b4fc4-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b4fc4-128">OUTPUTS</span></span>

### <span data-ttu-id="b4fc4-129">Microsoft. WindowsAzure. Storage. Table. SharedAccessTablePolicy</span><span class="sxs-lookup"><span data-stu-id="b4fc4-129">Microsoft.WindowsAzure.Storage.Table.SharedAccessTablePolicy</span></span>

## <span data-ttu-id="b4fc4-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="b4fc4-130">NOTES</span></span>

## <span data-ttu-id="b4fc4-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b4fc4-131">RELATED LINKS</span></span>

[<span data-ttu-id="b4fc4-132">Neu – AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b4fc4-132">New-AzStorageTableStoredAccessPolicy</span></span>](./New-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="b4fc4-133">Remove-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b4fc4-133">Remove-AzStorageTableStoredAccessPolicy</span></span>](./Remove-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="b4fc4-134">Satz-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b4fc4-134">Set-AzStorageTableStoredAccessPolicy</span></span>](./Set-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="b4fc4-135">Neu – AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="b4fc4-135">New-AzStorageContext</span></span>](./New-AzStorageContext.md)



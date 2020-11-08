---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FDD2CE98-6C7E-4B95-BA5B-B03B6AC6EAEF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountKey.md
ms.openlocfilehash: eebf58120449466ac18231af6daed538ff7da937
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177394"
---
# <span data-ttu-id="d0a11-101">New-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="d0a11-101">New-AzStorageAccountKey</span></span>

## <span data-ttu-id="d0a11-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d0a11-102">SYNOPSIS</span></span>
<span data-ttu-id="d0a11-103">Generiert einen Speicherschlüssel für ein Azure Storage-Konto erneut.</span><span class="sxs-lookup"><span data-stu-id="d0a11-103">Regenerates a storage key for an Azure Storage account.</span></span>

## <span data-ttu-id="d0a11-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d0a11-104">SYNTAX</span></span>

```
New-AzStorageAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d0a11-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d0a11-105">DESCRIPTION</span></span>
<span data-ttu-id="d0a11-106">Das Cmdlet **New-AzStorageAccountKey** generiert einen Speicherschlüssel für ein Azure Storage-Konto erneut.</span><span class="sxs-lookup"><span data-stu-id="d0a11-106">The **New-AzStorageAccountKey** cmdlet regenerates a storage key for an Azure Storage account.</span></span>

## <span data-ttu-id="d0a11-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d0a11-107">EXAMPLES</span></span>

### <span data-ttu-id="d0a11-108">Beispiel 1: Erneutes Generieren eines Speicher Schlüssels</span><span class="sxs-lookup"><span data-stu-id="d0a11-108">Example 1: Regenerate a storage key</span></span>
```
PS C:\>New-AzStorageAccountKey -ResourceGroupName "MyResourceGroup" -Name "mystorageaccount" -KeyName "key1"
```

<span data-ttu-id="d0a11-109">Mit diesem Befehl wird ein Speicherschlüssel für das angegebene Speicherkonto neu generiert.</span><span class="sxs-lookup"><span data-stu-id="d0a11-109">This command regenerates a storage key for the specified Storage account.</span></span>

## <span data-ttu-id="d0a11-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d0a11-110">PARAMETERS</span></span>

### <span data-ttu-id="d0a11-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0a11-111">-DefaultProfile</span></span>
<span data-ttu-id="d0a11-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d0a11-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0a11-113">-KeyName</span><span class="sxs-lookup"><span data-stu-id="d0a11-113">-KeyName</span></span>
<span data-ttu-id="d0a11-114">Gibt an, welche Taste neu generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="d0a11-114">Specifies which key to regenerate.</span></span>
<span data-ttu-id="d0a11-115">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="d0a11-115">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d0a11-116">key1</span><span class="sxs-lookup"><span data-stu-id="d0a11-116">key1</span></span>
- <span data-ttu-id="d0a11-117">key2</span><span class="sxs-lookup"><span data-stu-id="d0a11-117">key2</span></span>
- <span data-ttu-id="d0a11-118">kerb1</span><span class="sxs-lookup"><span data-stu-id="d0a11-118">kerb1</span></span>
- <span data-ttu-id="d0a11-119">kerb2</span><span class="sxs-lookup"><span data-stu-id="d0a11-119">kerb2</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: key1, key2, kerb1, kerb2

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0a11-120">-Name</span><span class="sxs-lookup"><span data-stu-id="d0a11-120">-Name</span></span>
<span data-ttu-id="d0a11-121">Gibt den Namen des speicherkontos an, für das ein Speicherschlüssel neu generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="d0a11-121">Specifies the name of the Storage account for which to regenerate a storage key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0a11-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0a11-122">-ResourceGroupName</span></span>
<span data-ttu-id="d0a11-123">Gibt den Namen der Ressourcengruppe an, die das Speicherkonto enthält.</span><span class="sxs-lookup"><span data-stu-id="d0a11-123">Specifies the name of the resource group that contains the Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0a11-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0a11-124">CommonParameters</span></span>
<span data-ttu-id="d0a11-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0a11-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0a11-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0a11-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0a11-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d0a11-127">INPUTS</span></span>

### <span data-ttu-id="d0a11-128">System. String</span><span class="sxs-lookup"><span data-stu-id="d0a11-128">System.String</span></span>

## <span data-ttu-id="d0a11-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d0a11-129">OUTPUTS</span></span>

### <span data-ttu-id="d0a11-130">Microsoft. Azure. Management. Storage. Models. StorageAccountListKeysResult</span><span class="sxs-lookup"><span data-stu-id="d0a11-130">Microsoft.Azure.Management.Storage.Models.StorageAccountListKeysResult</span></span>

## <span data-ttu-id="d0a11-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="d0a11-131">NOTES</span></span>

## <span data-ttu-id="d0a11-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d0a11-132">RELATED LINKS</span></span>

[<span data-ttu-id="d0a11-133">Get-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="d0a11-133">Get-AzStorageAccountKey</span></span>](./Get-AzStorageAccountKey.md)

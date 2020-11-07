---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FDD2CE98-6C7E-4B95-BA5B-B03B6AC6EAEF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/New-AzStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/New-AzStorageAccountKey.md
ms.openlocfilehash: 70acc17513e60892baae1fe8ebc15776518b3f57
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843028"
---
# <span data-ttu-id="8fb83-101">New-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="8fb83-101">New-AzStorageAccountKey</span></span>

## <span data-ttu-id="8fb83-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8fb83-102">SYNOPSIS</span></span>
<span data-ttu-id="8fb83-103">Generiert einen Speicherschlüssel für ein Azure Storage-Konto erneut.</span><span class="sxs-lookup"><span data-stu-id="8fb83-103">Regenerates a storage key for an Azure Storage account.</span></span>

## <span data-ttu-id="8fb83-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8fb83-104">SYNTAX</span></span>

```
New-AzStorageAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8fb83-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8fb83-105">DESCRIPTION</span></span>
<span data-ttu-id="8fb83-106">Das Cmdlet **New-AzStorageAccountKey** generiert einen Speicherschlüssel für ein Azure Storage-Konto erneut.</span><span class="sxs-lookup"><span data-stu-id="8fb83-106">The **New-AzStorageAccountKey** cmdlet regenerates a storage key for an Azure Storage account.</span></span>

## <span data-ttu-id="8fb83-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8fb83-107">EXAMPLES</span></span>

### <span data-ttu-id="8fb83-108">Beispiel 1: Erneutes Generieren eines Speicher Schlüssels</span><span class="sxs-lookup"><span data-stu-id="8fb83-108">Example 1: Regenerate a storage key</span></span>
```
PS C:\>New-AzStorageKey -ResourceGroupName "MyResourceGroup" -Name "mystorageaccount" -KeyName "key1"
```

<span data-ttu-id="8fb83-109">Mit diesem Befehl wird ein Speicherschlüssel für das angegebene Speicherkonto neu generiert.</span><span class="sxs-lookup"><span data-stu-id="8fb83-109">This command regenerates a storage key for the specified Storage account.</span></span>

## <span data-ttu-id="8fb83-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="8fb83-110">PARAMETERS</span></span>

### <span data-ttu-id="8fb83-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fb83-111">-DefaultProfile</span></span>
<span data-ttu-id="8fb83-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8fb83-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8fb83-113">-KeyName</span><span class="sxs-lookup"><span data-stu-id="8fb83-113">-KeyName</span></span>
<span data-ttu-id="8fb83-114">Gibt an, welche Taste neu generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="8fb83-114">Specifies which key to regenerate.</span></span>
<span data-ttu-id="8fb83-115">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="8fb83-115">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8fb83-116">key1</span><span class="sxs-lookup"><span data-stu-id="8fb83-116">key1</span></span>
- <span data-ttu-id="8fb83-117">key2</span><span class="sxs-lookup"><span data-stu-id="8fb83-117">key2</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: key1, key2

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fb83-118">-Name</span><span class="sxs-lookup"><span data-stu-id="8fb83-118">-Name</span></span>
<span data-ttu-id="8fb83-119">Gibt den Namen des speicherkontos an, für das ein Speicherschlüssel neu generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="8fb83-119">Specifies the name of the Storage account for which to regenerate a storage key.</span></span>

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

### <span data-ttu-id="8fb83-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8fb83-120">-ResourceGroupName</span></span>
<span data-ttu-id="8fb83-121">Gibt den Namen der Ressourcengruppe an, die das Speicherkonto enthält.</span><span class="sxs-lookup"><span data-stu-id="8fb83-121">Specifies the name of the resource group that contains the Storage account.</span></span>

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

### <span data-ttu-id="8fb83-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fb83-122">CommonParameters</span></span>
<span data-ttu-id="8fb83-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8fb83-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fb83-124">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8fb83-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fb83-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8fb83-125">INPUTS</span></span>

### <span data-ttu-id="8fb83-126">System. String</span><span class="sxs-lookup"><span data-stu-id="8fb83-126">System.String</span></span>

## <span data-ttu-id="8fb83-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8fb83-127">OUTPUTS</span></span>

### <span data-ttu-id="8fb83-128">Microsoft. Azure. Management. Storage. Models. StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="8fb83-128">Microsoft.Azure.Management.Storage.Models.StorageAccountKey</span></span>

## <span data-ttu-id="8fb83-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="8fb83-129">NOTES</span></span>

## <span data-ttu-id="8fb83-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8fb83-130">RELATED LINKS</span></span>

[<span data-ttu-id="8fb83-131">Get-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="8fb83-131">Get-AzStorageAccountKey</span></span>](./Get-AzStorageAccountKey.md)

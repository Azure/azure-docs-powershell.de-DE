---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: FDD2CE98-6C7E-4B95-BA5B-B03B6AC6EAEF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/new-azurermstorageaccountkey
schema: 2.0.0
ms.openlocfilehash: 7ea3847c011582d9be809f030a638b09b6cf9532
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848060"
---
# <span data-ttu-id="81fee-101">New-AzureRmStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="81fee-101">New-AzureRmStorageAccountKey</span></span>

## <span data-ttu-id="81fee-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="81fee-102">SYNOPSIS</span></span>
<span data-ttu-id="81fee-103">Generiert einen Speicherschlüssel für ein Azure Storage-Konto erneut.</span><span class="sxs-lookup"><span data-stu-id="81fee-103">Regenerates a storage key for an Azure Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="81fee-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="81fee-104">SYNTAX</span></span>

```
New-AzureRmStorageAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="81fee-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="81fee-105">DESCRIPTION</span></span>
<span data-ttu-id="81fee-106">Das Cmdlet **New-AzureRmStorageAccountKey** generiert einen Speicherschlüssel für ein Azure Storage-Konto erneut.</span><span class="sxs-lookup"><span data-stu-id="81fee-106">The **New-AzureRmStorageAccountKey** cmdlet regenerates a storage key for an Azure Storage account.</span></span>

## <span data-ttu-id="81fee-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="81fee-107">EXAMPLES</span></span>

### <span data-ttu-id="81fee-108">Beispiel 1: Erneutes Generieren eines Speicher Schlüssels</span><span class="sxs-lookup"><span data-stu-id="81fee-108">Example 1: Regenerate a storage key</span></span>
```
PS C:\>New-AzureRmStorageKey -ResourceGroupName "MyResourceGroup" -Name "mystorageaccount" -KeyName "key1"
```

<span data-ttu-id="81fee-109">Mit diesem Befehl wird ein Speicherschlüssel für das angegebene Speicherkonto neu generiert.</span><span class="sxs-lookup"><span data-stu-id="81fee-109">This command regenerates a storage key for the specified Storage account.</span></span>

## <span data-ttu-id="81fee-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="81fee-110">PARAMETERS</span></span>

### <span data-ttu-id="81fee-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81fee-111">-DefaultProfile</span></span>
<span data-ttu-id="81fee-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="81fee-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81fee-113">-KeyName</span><span class="sxs-lookup"><span data-stu-id="81fee-113">-KeyName</span></span>
<span data-ttu-id="81fee-114">Gibt an, welche Taste neu generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="81fee-114">Specifies which key to regenerate.</span></span>
<span data-ttu-id="81fee-115">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="81fee-115">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="81fee-116">key1</span><span class="sxs-lookup"><span data-stu-id="81fee-116">key1</span></span>
- <span data-ttu-id="81fee-117">key2</span><span class="sxs-lookup"><span data-stu-id="81fee-117">key2</span></span>

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

### <span data-ttu-id="81fee-118">-Name</span><span class="sxs-lookup"><span data-stu-id="81fee-118">-Name</span></span>
<span data-ttu-id="81fee-119">Gibt den Namen des speicherkontos an, für das ein Speicherschlüssel neu generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="81fee-119">Specifies the name of the Storage account for which to regenerate a storage key.</span></span>

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

### <span data-ttu-id="81fee-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81fee-120">-ResourceGroupName</span></span>
<span data-ttu-id="81fee-121">Gibt den Namen der Ressourcengruppe an, die das Speicherkonto enthält.</span><span class="sxs-lookup"><span data-stu-id="81fee-121">Specifies the name of the resource group that contains the Storage account.</span></span>

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

### <span data-ttu-id="81fee-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81fee-122">CommonParameters</span></span>
<span data-ttu-id="81fee-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81fee-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81fee-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81fee-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81fee-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="81fee-125">INPUTS</span></span>

### <span data-ttu-id="81fee-126">System. String</span><span class="sxs-lookup"><span data-stu-id="81fee-126">System.String</span></span>

## <span data-ttu-id="81fee-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="81fee-127">OUTPUTS</span></span>

### <span data-ttu-id="81fee-128">Microsoft. Azure. Management. Storage. Models. StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="81fee-128">Microsoft.Azure.Management.Storage.Models.StorageAccountKey</span></span>

## <span data-ttu-id="81fee-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="81fee-129">NOTES</span></span>

## <span data-ttu-id="81fee-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="81fee-130">RELATED LINKS</span></span>

[<span data-ttu-id="81fee-131">Get-AzureRmStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="81fee-131">Get-AzureRmStorageAccountKey</span></span>](./Get-AzureRmStorageAccountKey.md)

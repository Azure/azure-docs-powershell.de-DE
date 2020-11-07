---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/new-Azstorageaccountmanagementpolicyfilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountManagementPolicyFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountManagementPolicyFilter.md
ms.openlocfilehash: 3e4cc41bf67eaef505cdeb1e33f84753f20650a3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658833"
---
# <span data-ttu-id="320e6-101">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="320e6-101">New-AzStorageAccountManagementPolicyFilter</span></span>

## <span data-ttu-id="320e6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="320e6-102">SYNOPSIS</span></span>
<span data-ttu-id="320e6-103">Erstellt ein ManagementPolicy-Regelfilter Objekt, das in New-AzStorageAccountManagementPolicyRule verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="320e6-103">Creates a ManagementPolicy rule filter object, which can be used in New-AzStorageAccountManagementPolicyRule.</span></span>

## <span data-ttu-id="320e6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="320e6-104">SYNTAX</span></span>

```
New-AzStorageAccountManagementPolicyFilter [-PrefixMatch <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="320e6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="320e6-105">DESCRIPTION</span></span>
<span data-ttu-id="320e6-106">Mit dem Cmdlet **New-AzStorageAccountManagementPolicyFilter** wird ein ManagementPolicy-Regelfilter Objekt erstellt, das in New-AzStorageAccountManagementPolicyRule verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="320e6-106">The **New-AzStorageAccountManagementPolicyFilter** cmdlet creates a ManagementPolicy rule filter object, which can be used in New-AzStorageAccountManagementPolicyRule.</span></span>

## <span data-ttu-id="320e6-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="320e6-107">EXAMPLES</span></span>

### <span data-ttu-id="320e6-108">Beispiel 1: erstellt ein ManagementPolicy-Regelfilter Objekt, fügt es dann einer Verwaltungsrichtlinien Regel hinzu und legt es auf ein Speicherkonto</span><span class="sxs-lookup"><span data-stu-id="320e6-108">Example 1: Creates a ManagementPolicy rule filter object, then add it to a management policy rule and set to a Storage account</span></span>
```
PS C:\>$filter = New-AzStorageAccountManagementPolicyFilter -PrefixMatch blobprefix1,blobprefix2
PS C:\>$filter 

PrefixMatch                BlobTypes  
-----------                ---------  
{blobprefix1, blobprefix2} {blockBlob}

PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction Delete -daysAfterModificationGreaterThan 100
PS C:\>$rule = New-AzStorageAccountManagementPolicyRule -Name Test -Action $action -Filter $filter
PS C:\>$policy = Set-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Rule $rule
```

<span data-ttu-id="320e6-109">Mit diesem Befehl wird ein ManagementPolicy-Regelfilter Objekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="320e6-109">This command create a ManagementPolicy rule filter object.</span></span> <span data-ttu-id="320e6-110">Fügen Sie es dann einer Verwaltungsrichtlinien Regel hinzu, und legen Sie es auf ein Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="320e6-110">Then add it to a management policy rule and set to a Storage account.</span></span>

## <span data-ttu-id="320e6-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="320e6-111">PARAMETERS</span></span>

### <span data-ttu-id="320e6-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="320e6-112">-DefaultProfile</span></span>
<span data-ttu-id="320e6-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="320e6-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="320e6-114">-PrefixMatch</span><span class="sxs-lookup"><span data-stu-id="320e6-114">-PrefixMatch</span></span>
<span data-ttu-id="320e6-115">Ein Array von Zeichenfolgen für Präfixe, die übereinstimmen sollen.</span><span class="sxs-lookup"><span data-stu-id="320e6-115">An array of strings for prefixes to be match.</span></span>
<span data-ttu-id="320e6-116">Eine Präfixzeichenfolge muss mit einem Containernamen beginnen.</span><span class="sxs-lookup"><span data-stu-id="320e6-116">A prefix string must start with a container name.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="320e6-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="320e6-117">CommonParameters</span></span>
<span data-ttu-id="320e6-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="320e6-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="320e6-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="320e6-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="320e6-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="320e6-120">INPUTS</span></span>

### <span data-ttu-id="320e6-121">Keine</span><span class="sxs-lookup"><span data-stu-id="320e6-121">None</span></span>

## <span data-ttu-id="320e6-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="320e6-122">OUTPUTS</span></span>

### <span data-ttu-id="320e6-123">Microsoft. Azure. Commands. Management. Storage. Models. PSManagementPolicyRuleFilter</span><span class="sxs-lookup"><span data-stu-id="320e6-123">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyRuleFilter</span></span>

## <span data-ttu-id="320e6-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="320e6-124">NOTES</span></span>

## <span data-ttu-id="320e6-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="320e6-125">RELATED LINKS</span></span>

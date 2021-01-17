---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/new-Azstorageaccountmanagementpolicyfilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountManagementPolicyFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountManagementPolicyFilter.md
ms.openlocfilehash: 48ae8b87671e52abe4d109025048fe1e4aeca117
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98290506"
---
# <span data-ttu-id="fc845-101">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="fc845-101">New-AzStorageAccountManagementPolicyFilter</span></span>

## <span data-ttu-id="fc845-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc845-102">SYNOPSIS</span></span>
<span data-ttu-id="fc845-103">Erstellt ein ManagementPolicy-Regelfilterobjekt, das in "New-AzStorageAccountManagementPolicyRule" verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="fc845-103">Creates a ManagementPolicy rule filter object, which can be used in New-AzStorageAccountManagementPolicyRule.</span></span>

## <span data-ttu-id="fc845-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fc845-104">SYNTAX</span></span>

```
New-AzStorageAccountManagementPolicyFilter [-PrefixMatch <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fc845-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fc845-105">DESCRIPTION</span></span>
<span data-ttu-id="fc845-106">Das **Cmdlet "New-AzStorageAccountManagementPolicyFilter"** erstellt ein ManagementPolicy-Regelfilterobjekt, das in "New-AzStorageAccountManagementPolicyRule" verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="fc845-106">The **New-AzStorageAccountManagementPolicyFilter** cmdlet creates a ManagementPolicy rule filter object, which can be used in New-AzStorageAccountManagementPolicyRule.</span></span>

## <span data-ttu-id="fc845-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fc845-107">EXAMPLES</span></span>

### <span data-ttu-id="fc845-108">Beispiel 1: Erstellt ein Verwaltungsrichtlinienfilterobjekt, fügt es einer Verwaltungsrichtlinienregel hinzu und legt es auf ein Speicherkonto festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fc845-108">Example 1: Creates a ManagementPolicy rule filter object, then add it to a management policy rule and set to a Storage account</span></span>
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

<span data-ttu-id="fc845-109">Mit diesem Befehl wird ein Filterobjekt für eine Verwaltungsregel erstellt.</span><span class="sxs-lookup"><span data-stu-id="fc845-109">This command create a ManagementPolicy rule filter object.</span></span> <span data-ttu-id="fc845-110">Fügen Sie sie dann einer Verwaltungsrichtlinienregel hinzu, und legen Sie sie auf ein Speicherkonto festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fc845-110">Then add it to a management policy rule and set to a Storage account.</span></span>

## <span data-ttu-id="fc845-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fc845-111">PARAMETERS</span></span>

### <span data-ttu-id="fc845-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc845-112">-DefaultProfile</span></span>
<span data-ttu-id="fc845-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fc845-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc845-114">-PrefixMatch</span><span class="sxs-lookup"><span data-stu-id="fc845-114">-PrefixMatch</span></span>
<span data-ttu-id="fc845-115">Ein Array von Zeichenfolgen für die zu matching-Präfixe.</span><span class="sxs-lookup"><span data-stu-id="fc845-115">An array of strings for prefixes to be match.</span></span>
<span data-ttu-id="fc845-116">Eine Präfixzeichenfolge muss mit einem Containernamen beginnen.</span><span class="sxs-lookup"><span data-stu-id="fc845-116">A prefix string must start with a container name.</span></span>

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

### <span data-ttu-id="fc845-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc845-117">CommonParameters</span></span>
<span data-ttu-id="fc845-118">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc845-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc845-119">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc845-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc845-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fc845-120">INPUTS</span></span>

### <span data-ttu-id="fc845-121">Keine</span><span class="sxs-lookup"><span data-stu-id="fc845-121">None</span></span>

## <span data-ttu-id="fc845-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fc845-122">OUTPUTS</span></span>

### <span data-ttu-id="fc845-123">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyRuleFilter</span><span class="sxs-lookup"><span data-stu-id="fc845-123">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyRuleFilter</span></span>

## <span data-ttu-id="fc845-124">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="fc845-124">NOTES</span></span>

## <span data-ttu-id="fc845-125">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="fc845-125">RELATED LINKS</span></span>

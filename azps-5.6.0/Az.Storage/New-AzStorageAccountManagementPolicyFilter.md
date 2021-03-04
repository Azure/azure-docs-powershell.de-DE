---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/Az.storage/new-Azstorageaccountmanagementpolicyfilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountManagementPolicyFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountManagementPolicyFilter.md
ms.openlocfilehash: 40a2420803197b21bb9f0f8d20b771482b4e694b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101944573"
---
# <span data-ttu-id="ffa71-101">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="ffa71-101">New-AzStorageAccountManagementPolicyFilter</span></span>

## <span data-ttu-id="ffa71-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ffa71-102">SYNOPSIS</span></span>
<span data-ttu-id="ffa71-103">Erstellt ein ManagementPolicy-Regelfilterobjekt, das in New-AzStorageAccountManagementPolicyRule verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="ffa71-103">Creates a ManagementPolicy rule filter object, which can be used in New-AzStorageAccountManagementPolicyRule.</span></span>

## <span data-ttu-id="ffa71-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ffa71-104">SYNTAX</span></span>

```
New-AzStorageAccountManagementPolicyFilter [-PrefixMatch <String[]>] [-BlobType <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ffa71-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ffa71-105">DESCRIPTION</span></span>
<span data-ttu-id="ffa71-106">Das **Cmdlet New-AzStorageAccountManagementPolicyFilter** erstellt ein ManagementPolicy-Regelfilterobjekt, das in New-AzStorageAccountManagementPolicyRule verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="ffa71-106">The **New-AzStorageAccountManagementPolicyFilter** cmdlet creates a ManagementPolicy rule filter object, which can be used in New-AzStorageAccountManagementPolicyRule.</span></span>

## <span data-ttu-id="ffa71-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ffa71-107">EXAMPLES</span></span>

### <span data-ttu-id="ffa71-108">Beispiel 1: Erstellt ein ManagementPolicy-Regelfilterobjekt, fügt es dann einer Verwaltungsrichtlinienregel hinzu und legt es auf ein Speicherkonto an.</span><span class="sxs-lookup"><span data-stu-id="ffa71-108">Example 1: Creates a ManagementPolicy rule filter object, then add it to a management policy rule and set to a Storage account</span></span>
```
PS C:\>$filter = New-AzStorageAccountManagementPolicyFilter -PrefixMatch blobprefix1,blobprefix2 -BlobType appendBlob,blockBlob
PS C:\>$filter 

PrefixMatch                BlobTypes  
-----------                ---------  
{blobprefix1, blobprefix2} {appendBlob, blockBlob}

PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction Delete -daysAfterModificationGreaterThan 100
PS C:\>$rule = New-AzStorageAccountManagementPolicyRule -Name Test -Action $action -Filter $filter
PS C:\>$policy = Set-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Rule $rule
```

<span data-ttu-id="ffa71-109">Mit diesem Befehl wird ein ManagementPolicy-Regelfilterobjekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="ffa71-109">This command create a ManagementPolicy rule filter object.</span></span> <span data-ttu-id="ffa71-110">Fügen Sie sie dann einer Verwaltungsrichtlinienregel hinzu, und legen Sie sie auf ein Speicherkonto festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ffa71-110">Then add it to a management policy rule and set to a Storage account.</span></span>

## <span data-ttu-id="ffa71-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="ffa71-111">PARAMETERS</span></span>

### <span data-ttu-id="ffa71-112">-BlobType</span><span class="sxs-lookup"><span data-stu-id="ffa71-112">-BlobType</span></span>
<span data-ttu-id="ffa71-113">Ein Array von Zeichenfolgen für blobtypes, die übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="ffa71-113">An array of strings for blobtypes to be match.</span></span> <span data-ttu-id="ffa71-114">Derzeit unterstützt blockBlob alle Gestuft- und Löschaktionen.</span><span class="sxs-lookup"><span data-stu-id="ffa71-114">Currently blockBlob supports all tiering and delete actions.</span></span> <span data-ttu-id="ffa71-115">Für appendBlob werden nur Löschaktionen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ffa71-115">Only delete actions are supported for appendBlob.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: blockBlob, appendBlob

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffa71-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffa71-116">-DefaultProfile</span></span>
<span data-ttu-id="ffa71-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ffa71-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ffa71-118">-PrefixMatch</span><span class="sxs-lookup"><span data-stu-id="ffa71-118">-PrefixMatch</span></span>
<span data-ttu-id="ffa71-119">Ein Array von Zeichenfolgen für zu übereinstimmende Präfixe.</span><span class="sxs-lookup"><span data-stu-id="ffa71-119">An array of strings for prefixes to be match.</span></span>
<span data-ttu-id="ffa71-120">Eine Präfixzeichenfolge muss mit einem Containernamen beginnen.</span><span class="sxs-lookup"><span data-stu-id="ffa71-120">A prefix string must start with a container name.</span></span>

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

### <span data-ttu-id="ffa71-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffa71-121">CommonParameters</span></span>
<span data-ttu-id="ffa71-122">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ffa71-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffa71-123">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ffa71-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffa71-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ffa71-124">INPUTS</span></span>

### <span data-ttu-id="ffa71-125">Keine</span><span class="sxs-lookup"><span data-stu-id="ffa71-125">None</span></span>

## <span data-ttu-id="ffa71-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ffa71-126">OUTPUTS</span></span>

### <span data-ttu-id="ffa71-127">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyRuleFilter</span><span class="sxs-lookup"><span data-stu-id="ffa71-127">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyRuleFilter</span></span>

## <span data-ttu-id="ffa71-128">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="ffa71-128">NOTES</span></span>

## <span data-ttu-id="ffa71-129">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="ffa71-129">RELATED LINKS</span></span>

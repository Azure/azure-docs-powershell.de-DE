---
external help file: Microsoft.Azure.Commands.ManagementPartner.dll-Help.xml
Module Name: AzureRM.ManagementPartner
online version: https://docs.microsoft.com/en-us/powershell/module/get-azurermmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagementPartner/Commands.Partner/help/Get-AzureRmManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagementPartner/Commands.Partner/help/Get-AzureRmManagementPartner.md
ms.openlocfilehash: b1fe94533074860a3c95c05d6609bb8ebb446a9b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497590"
---
# <span data-ttu-id="da6a4-101">Get-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="da6a4-101">Get-AzureRmManagementPartner</span></span>

## <span data-ttu-id="da6a4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="da6a4-102">SYNOPSIS</span></span>
<span data-ttu-id="da6a4-103">Ruft die Microsoft-Partner Netzwerk (MPN)-ID des aktuellen authentifizierten Benutzers oder Dienst Prinzipals ab.</span><span class="sxs-lookup"><span data-stu-id="da6a4-103">Gets the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="da6a4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="da6a4-104">SYNTAX</span></span>

```
Get-AzureRmManagementPartner [[-PartnerId] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="da6a4-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="da6a4-105">DESCRIPTION</span></span>
<span data-ttu-id="da6a4-106">Ruft die Microsoft-Partner Netzwerk (MPN)-ID des aktuellen authentifizierten Benutzers oder Dienst Prinzipals ab.</span><span class="sxs-lookup"><span data-stu-id="da6a4-106">Gets the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span> 

## <span data-ttu-id="da6a4-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="da6a4-107">EXAMPLES</span></span>

### <span data-ttu-id="da6a4-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="da6a4-108">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmManagementPartner
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="da6a4-109">Abrufen der aktuellen Management-Partner-ID</span><span class="sxs-lookup"><span data-stu-id="da6a4-109">Get the current management partner id</span></span>

### <span data-ttu-id="da6a4-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="da6a4-110">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmManagementPartner -PartnerId 4977985
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="da6a4-111">Abrufen der aktuellen Management-Partner-ID mithilfe einer Partner-ID, wenn Sie nicht übereinstimmen, schlägt Sie fehl</span><span class="sxs-lookup"><span data-stu-id="da6a4-111">Get the current management partner id using a partner id, if they don't match, it will fail</span></span>

## <span data-ttu-id="da6a4-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="da6a4-112">PARAMETERS</span></span>

### <span data-ttu-id="da6a4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da6a4-113">-DefaultProfile</span></span>
<span data-ttu-id="da6a4-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="da6a4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da6a4-115">-Partner-Nr</span><span class="sxs-lookup"><span data-stu-id="da6a4-115">-PartnerId</span></span>
<span data-ttu-id="da6a4-116">Die VERWALTUNGSPARTNER-ID ist eine sechsstellige Zahl</span><span class="sxs-lookup"><span data-stu-id="da6a4-116">The management partner id, it is a 6 digits number</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da6a4-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da6a4-117">CommonParameters</span></span>
<span data-ttu-id="da6a4-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da6a4-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da6a4-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da6a4-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da6a4-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="da6a4-120">INPUTS</span></span>

### <span data-ttu-id="da6a4-121">Keine</span><span class="sxs-lookup"><span data-stu-id="da6a4-121">None</span></span>

## <span data-ttu-id="da6a4-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="da6a4-122">OUTPUTS</span></span>

### <span data-ttu-id="da6a4-123">Microsoft. Azure. Commands. resources. PSManagementPartner</span><span class="sxs-lookup"><span data-stu-id="da6a4-123">Microsoft.Azure.Commands.Resources.PSManagementPartner</span></span>

## <span data-ttu-id="da6a4-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="da6a4-124">NOTES</span></span>

## <span data-ttu-id="da6a4-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="da6a4-125">RELATED LINKS</span></span>

[<span data-ttu-id="da6a4-126">Remove-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="da6a4-126">Remove-AzureRmManagementPartner</span></span>](./Remove-AzureRmManagementPartner.md)

[<span data-ttu-id="da6a4-127">Neu – AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="da6a4-127">New-AzureRmManagementPartner</span></span>](./New-AzureRmManagementPartner.md)

[<span data-ttu-id="da6a4-128">Update-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="da6a4-128">Update-AzureRmManagementPartner</span></span>](./Update-AzureRmManagementPartner.md)

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagementPartner.dll-Help.xml
Module Name: Az.ManagementPartner
online version: https://docs.microsoft.com/powershell/module/az.managementpartner/get-azmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Get-AzManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Get-AzManagementPartner.md
ms.openlocfilehash: e09e63ed68ac87156fd03f73c992043b8a0271cf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934155"
---
# <span data-ttu-id="e7fe5-101">Get-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="e7fe5-101">Get-AzManagementPartner</span></span>

## <span data-ttu-id="e7fe5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7fe5-102">SYNOPSIS</span></span>
<span data-ttu-id="e7fe5-103">Ruft die Microsoft Partner Network(MPN)-ID des aktuellen authentifizierten Benutzers oder Dienstprinzipals ab.</span><span class="sxs-lookup"><span data-stu-id="e7fe5-103">Gets the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="e7fe5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e7fe5-104">SYNTAX</span></span>

```
Get-AzManagementPartner [[-PartnerId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e7fe5-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e7fe5-105">DESCRIPTION</span></span>
<span data-ttu-id="e7fe5-106">Ruft die Microsoft Partner Network(MPN)-ID des aktuellen authentifizierten Benutzers oder Dienstprinzipals ab.</span><span class="sxs-lookup"><span data-stu-id="e7fe5-106">Gets the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="e7fe5-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e7fe5-107">EXAMPLES</span></span>

### <span data-ttu-id="e7fe5-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e7fe5-108">Example 1</span></span>
```powershell
PS C:\> Get-AzManagementPartner
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="e7fe5-109">Holen Sie sich die aktuelle Managementpartner-ID</span><span class="sxs-lookup"><span data-stu-id="e7fe5-109">Get the current management partner id</span></span>

### <span data-ttu-id="e7fe5-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="e7fe5-110">Example 2</span></span>
```powershell
PS C:\> Get-AzManagementPartner -PartnerId 4977985
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="e7fe5-111">Holen Sie sich die aktuelle Managementpartner-ID mithilfe einer Partner-ID, wenn sie nicht übereinstimmen, ist dies nicht der Fehler.</span><span class="sxs-lookup"><span data-stu-id="e7fe5-111">Get the current management partner id using a partner id, if they don't match, it will fail</span></span>

## <span data-ttu-id="e7fe5-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="e7fe5-112">PARAMETERS</span></span>

### <span data-ttu-id="e7fe5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7fe5-113">-DefaultProfile</span></span>
<span data-ttu-id="e7fe5-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e7fe5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7fe5-115">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="e7fe5-115">-PartnerId</span></span>
<span data-ttu-id="e7fe5-116">Die Id des Managementpartners ist eine 6-stellige Zahl.</span><span class="sxs-lookup"><span data-stu-id="e7fe5-116">The management partner id, it is a 6 digits number</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7fe5-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7fe5-117">CommonParameters</span></span>
<span data-ttu-id="e7fe5-118">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7fe5-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7fe5-119">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7fe5-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7fe5-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e7fe5-120">INPUTS</span></span>

### <span data-ttu-id="e7fe5-121">Keine</span><span class="sxs-lookup"><span data-stu-id="e7fe5-121">None</span></span>

## <span data-ttu-id="e7fe5-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e7fe5-122">OUTPUTS</span></span>

### <span data-ttu-id="e7fe5-123">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span><span class="sxs-lookup"><span data-stu-id="e7fe5-123">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span></span>

## <span data-ttu-id="e7fe5-124">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="e7fe5-124">NOTES</span></span>

## <span data-ttu-id="e7fe5-125">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="e7fe5-125">RELATED LINKS</span></span>

[<span data-ttu-id="e7fe5-126">Remove-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="e7fe5-126">Remove-AzManagementPartner</span></span>](./Remove-AzManagementPartner.md)

[<span data-ttu-id="e7fe5-127">New-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="e7fe5-127">New-AzManagementPartner</span></span>](./New-AzManagementPartner.md)

[<span data-ttu-id="e7fe5-128">Update-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="e7fe5-128">Update-AzManagementPartner</span></span>](./Update-AzManagementPartner.md)
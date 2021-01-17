---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagementPartner.dll-Help.xml
Module Name: Az.ManagementPartner
online version: https://docs.microsoft.com/en-us/powershell/module/az.managementpartner/get-azmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Get-AzManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Get-AzManagementPartner.md
ms.openlocfilehash: 1031c9c8828969d16097953aa7440e2c8c0a8c1b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470425"
---
# <span data-ttu-id="c7d3d-101">Get-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="c7d3d-101">Get-AzManagementPartner</span></span>

## <span data-ttu-id="c7d3d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7d3d-102">SYNOPSIS</span></span>
<span data-ttu-id="c7d3d-103">Ruft die Microsoft Partner Network(MPN)-ID des aktuell authentifizierten Benutzers oder Dienstprinzipal ab.</span><span class="sxs-lookup"><span data-stu-id="c7d3d-103">Gets the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="c7d3d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c7d3d-104">SYNTAX</span></span>

```
Get-AzManagementPartner [[-PartnerId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7d3d-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c7d3d-105">DESCRIPTION</span></span>
<span data-ttu-id="c7d3d-106">Ruft die Microsoft Partner Network(MPN)-ID des aktuell authentifizierten Benutzers oder Dienstprinzipal ab.</span><span class="sxs-lookup"><span data-stu-id="c7d3d-106">Gets the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="c7d3d-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c7d3d-107">EXAMPLES</span></span>

### <span data-ttu-id="c7d3d-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c7d3d-108">Example 1</span></span>
```powershell
PS C:\> Get-AzManagementPartner
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="c7d3d-109">Holen Sie sich die aktuelle Managementpartner-ID.</span><span class="sxs-lookup"><span data-stu-id="c7d3d-109">Get the current management partner id</span></span>

### <span data-ttu-id="c7d3d-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="c7d3d-110">Example 2</span></span>
```powershell
PS C:\> Get-AzManagementPartner -PartnerId 4977985
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="c7d3d-111">Holen Sie sich die id des aktuellen Managementpartners mithilfe einer Partner-ID. Wenn sie nicht übereinstimmen, kann sie nicht gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="c7d3d-111">Get the current management partner id using a partner id, if they don't match, it will fail</span></span>

## <span data-ttu-id="c7d3d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c7d3d-112">PARAMETERS</span></span>

### <span data-ttu-id="c7d3d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7d3d-113">-DefaultProfile</span></span>
<span data-ttu-id="c7d3d-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c7d3d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7d3d-115">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="c7d3d-115">-PartnerId</span></span>
<span data-ttu-id="c7d3d-116">Die 6-stellige Nummer des Managementpartners</span><span class="sxs-lookup"><span data-stu-id="c7d3d-116">The management partner id, it is a 6 digits number</span></span>

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

### <span data-ttu-id="c7d3d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7d3d-117">CommonParameters</span></span>
<span data-ttu-id="c7d3d-118">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7d3d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7d3d-119">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7d3d-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7d3d-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c7d3d-120">INPUTS</span></span>

### <span data-ttu-id="c7d3d-121">Keine</span><span class="sxs-lookup"><span data-stu-id="c7d3d-121">None</span></span>

## <span data-ttu-id="c7d3d-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c7d3d-122">OUTPUTS</span></span>

### <span data-ttu-id="c7d3d-123">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span><span class="sxs-lookup"><span data-stu-id="c7d3d-123">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span></span>

## <span data-ttu-id="c7d3d-124">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c7d3d-124">NOTES</span></span>

## <span data-ttu-id="c7d3d-125">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c7d3d-125">RELATED LINKS</span></span>

[<span data-ttu-id="c7d3d-126">Remove-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="c7d3d-126">Remove-AzManagementPartner</span></span>](./Remove-AzManagementPartner.md)

[<span data-ttu-id="c7d3d-127">New-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="c7d3d-127">New-AzManagementPartner</span></span>](./New-AzManagementPartner.md)

[<span data-ttu-id="c7d3d-128">Update-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="c7d3d-128">Update-AzManagementPartner</span></span>](./Update-AzManagementPartner.md)
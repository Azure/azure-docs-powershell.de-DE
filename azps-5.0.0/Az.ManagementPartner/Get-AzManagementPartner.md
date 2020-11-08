---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagementPartner.dll-Help.xml
Module Name: Az.ManagementPartner
online version: https://docs.microsoft.com/en-us/powershell/module/az.managementpartner/get-azmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Get-AzManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Get-AzManagementPartner.md
ms.openlocfilehash: 1031c9c8828969d16097953aa7440e2c8c0a8c1b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177535"
---
# <span data-ttu-id="c6e02-101">Get-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="c6e02-101">Get-AzManagementPartner</span></span>

## <span data-ttu-id="c6e02-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c6e02-102">SYNOPSIS</span></span>
<span data-ttu-id="c6e02-103">Ruft die Microsoft-Partner Netzwerk (MPN)-ID des aktuellen authentifizierten Benutzers oder Dienst Prinzipals ab.</span><span class="sxs-lookup"><span data-stu-id="c6e02-103">Gets the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="c6e02-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c6e02-104">SYNTAX</span></span>

```
Get-AzManagementPartner [[-PartnerId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c6e02-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c6e02-105">DESCRIPTION</span></span>
<span data-ttu-id="c6e02-106">Ruft die Microsoft-Partner Netzwerk (MPN)-ID des aktuellen authentifizierten Benutzers oder Dienst Prinzipals ab.</span><span class="sxs-lookup"><span data-stu-id="c6e02-106">Gets the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="c6e02-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c6e02-107">EXAMPLES</span></span>

### <span data-ttu-id="c6e02-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c6e02-108">Example 1</span></span>
```powershell
PS C:\> Get-AzManagementPartner
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="c6e02-109">Abrufen der aktuellen Management-Partner-ID</span><span class="sxs-lookup"><span data-stu-id="c6e02-109">Get the current management partner id</span></span>

### <span data-ttu-id="c6e02-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="c6e02-110">Example 2</span></span>
```powershell
PS C:\> Get-AzManagementPartner -PartnerId 4977985
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="c6e02-111">Abrufen der aktuellen Management-Partner-ID mithilfe einer Partner-ID, wenn Sie nicht übereinstimmen, schlägt Sie fehl</span><span class="sxs-lookup"><span data-stu-id="c6e02-111">Get the current management partner id using a partner id, if they don't match, it will fail</span></span>

## <span data-ttu-id="c6e02-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="c6e02-112">PARAMETERS</span></span>

### <span data-ttu-id="c6e02-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6e02-113">-DefaultProfile</span></span>
<span data-ttu-id="c6e02-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c6e02-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6e02-115">-Partner-Nr</span><span class="sxs-lookup"><span data-stu-id="c6e02-115">-PartnerId</span></span>
<span data-ttu-id="c6e02-116">Die VERWALTUNGSPARTNER-ID ist eine sechsstellige Zahl</span><span class="sxs-lookup"><span data-stu-id="c6e02-116">The management partner id, it is a 6 digits number</span></span>

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

### <span data-ttu-id="c6e02-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6e02-117">CommonParameters</span></span>
<span data-ttu-id="c6e02-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6e02-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6e02-119">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6e02-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6e02-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c6e02-120">INPUTS</span></span>

### <span data-ttu-id="c6e02-121">Keine</span><span class="sxs-lookup"><span data-stu-id="c6e02-121">None</span></span>

## <span data-ttu-id="c6e02-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c6e02-122">OUTPUTS</span></span>

### <span data-ttu-id="c6e02-123">Microsoft. Azure. Commands. ManagementPartner. PSManagementPartner</span><span class="sxs-lookup"><span data-stu-id="c6e02-123">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span></span>

## <span data-ttu-id="c6e02-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="c6e02-124">NOTES</span></span>

## <span data-ttu-id="c6e02-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c6e02-125">RELATED LINKS</span></span>

[<span data-ttu-id="c6e02-126">Remove-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="c6e02-126">Remove-AzManagementPartner</span></span>](./Remove-AzManagementPartner.md)

[<span data-ttu-id="c6e02-127">Neu – AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="c6e02-127">New-AzManagementPartner</span></span>](./New-AzManagementPartner.md)

[<span data-ttu-id="c6e02-128">Update-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="c6e02-128">Update-AzManagementPartner</span></span>](./Update-AzManagementPartner.md)
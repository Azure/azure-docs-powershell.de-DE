---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagementPartner.dll-Help.xml
Module Name: Az.ManagementPartner
online version: https://docs.microsoft.com/en-us/powershell/module/az.managementpartner/get-azmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Get-AzManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Get-AzManagementPartner.md
ms.openlocfilehash: 1031c9c8828969d16097953aa7440e2c8c0a8c1b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009766"
---
# <span data-ttu-id="b7323-101">Get-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="b7323-101">Get-AzManagementPartner</span></span>

## <span data-ttu-id="b7323-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b7323-102">SYNOPSIS</span></span>
<span data-ttu-id="b7323-103">Ruft die Microsoft-Partner Netzwerk (MPN)-ID des aktuellen authentifizierten Benutzers oder Dienst Prinzipals ab.</span><span class="sxs-lookup"><span data-stu-id="b7323-103">Gets the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="b7323-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b7323-104">SYNTAX</span></span>

```
Get-AzManagementPartner [[-PartnerId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b7323-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b7323-105">DESCRIPTION</span></span>
<span data-ttu-id="b7323-106">Ruft die Microsoft-Partner Netzwerk (MPN)-ID des aktuellen authentifizierten Benutzers oder Dienst Prinzipals ab.</span><span class="sxs-lookup"><span data-stu-id="b7323-106">Gets the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="b7323-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b7323-107">EXAMPLES</span></span>

### <span data-ttu-id="b7323-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b7323-108">Example 1</span></span>
```powershell
PS C:\> Get-AzManagementPartner
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="b7323-109">Abrufen der aktuellen Management-Partner-ID</span><span class="sxs-lookup"><span data-stu-id="b7323-109">Get the current management partner id</span></span>

### <span data-ttu-id="b7323-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="b7323-110">Example 2</span></span>
```powershell
PS C:\> Get-AzManagementPartner -PartnerId 4977985
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="b7323-111">Abrufen der aktuellen Management-Partner-ID mithilfe einer Partner-ID, wenn Sie nicht übereinstimmen, schlägt Sie fehl</span><span class="sxs-lookup"><span data-stu-id="b7323-111">Get the current management partner id using a partner id, if they don't match, it will fail</span></span>

## <span data-ttu-id="b7323-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="b7323-112">PARAMETERS</span></span>

### <span data-ttu-id="b7323-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7323-113">-DefaultProfile</span></span>
<span data-ttu-id="b7323-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b7323-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7323-115">-Partner-Nr</span><span class="sxs-lookup"><span data-stu-id="b7323-115">-PartnerId</span></span>
<span data-ttu-id="b7323-116">Die VERWALTUNGSPARTNER-ID ist eine sechsstellige Zahl</span><span class="sxs-lookup"><span data-stu-id="b7323-116">The management partner id, it is a 6 digits number</span></span>

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

### <span data-ttu-id="b7323-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7323-117">CommonParameters</span></span>
<span data-ttu-id="b7323-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7323-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7323-119">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7323-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7323-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b7323-120">INPUTS</span></span>

### <span data-ttu-id="b7323-121">Keine</span><span class="sxs-lookup"><span data-stu-id="b7323-121">None</span></span>

## <span data-ttu-id="b7323-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b7323-122">OUTPUTS</span></span>

### <span data-ttu-id="b7323-123">Microsoft. Azure. Commands. ManagementPartner. PSManagementPartner</span><span class="sxs-lookup"><span data-stu-id="b7323-123">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span></span>

## <span data-ttu-id="b7323-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="b7323-124">NOTES</span></span>

## <span data-ttu-id="b7323-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b7323-125">RELATED LINKS</span></span>

[<span data-ttu-id="b7323-126">Remove-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="b7323-126">Remove-AzManagementPartner</span></span>](./Remove-AzManagementPartner.md)

[<span data-ttu-id="b7323-127">Neu – AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="b7323-127">New-AzManagementPartner</span></span>](./New-AzManagementPartner.md)

[<span data-ttu-id="b7323-128">Update-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="b7323-128">Update-AzManagementPartner</span></span>](./Update-AzManagementPartner.md)
---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagementPartner.dll-Help.xml
Module Name: Az.ManagementPartner
online version: https://docs.microsoft.com/en-us/powershell/module/az.managementpartner/new-azmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/New-AzManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/New-AzManagementPartner.md
ms.openlocfilehash: 9e6c56fa48b71e2571b7702e170bdc3e9e41f3aa
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467635"
---
# <span data-ttu-id="828bb-101">New-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="828bb-101">New-AzManagementPartner</span></span>

## <span data-ttu-id="828bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="828bb-102">SYNOPSIS</span></span>
<span data-ttu-id="828bb-103">Ordnet dem aktuell authentifizierten Benutzer oder Dienstprinzipal eine MICROSOFT Partner Network(MPN)-ID zu.</span><span class="sxs-lookup"><span data-stu-id="828bb-103">Associates a Microsoft Partner Network(MPN) ID to the current authenticated user or service principal.</span></span>

## <span data-ttu-id="828bb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="828bb-104">SYNTAX</span></span>

```
New-AzManagementPartner [-PartnerId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="828bb-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="828bb-105">DESCRIPTION</span></span>
<span data-ttu-id="828bb-106">Ordnet dem aktuell authentifizierten Benutzer oder Dienstprinzipal eine MICROSOFT Partner Network(MPN)-ID zu.</span><span class="sxs-lookup"><span data-stu-id="828bb-106">Associates a Microsoft Partner Network(MPN) ID to the current authenticated user or service principal.</span></span>

## <span data-ttu-id="828bb-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="828bb-107">EXAMPLES</span></span>

### <span data-ttu-id="828bb-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="828bb-108">Example 1</span></span>
```powershell
PS C:\> New-AzManagementPartner -PartnerId 4977985
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="828bb-109">Hinzufügen eines Managementpartners</span><span class="sxs-lookup"><span data-stu-id="828bb-109">Add a management partner</span></span>

## <span data-ttu-id="828bb-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="828bb-110">PARAMETERS</span></span>

### <span data-ttu-id="828bb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="828bb-111">-DefaultProfile</span></span>
<span data-ttu-id="828bb-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="828bb-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="828bb-113">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="828bb-113">-PartnerId</span></span>
<span data-ttu-id="828bb-114">Die 6-stellige Nummer des Managementpartners</span><span class="sxs-lookup"><span data-stu-id="828bb-114">The management partner id, it is a 6 digits number</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="828bb-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="828bb-115">-Confirm</span></span>
<span data-ttu-id="828bb-116">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="828bb-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="828bb-117">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="828bb-117">-WhatIf</span></span>
<span data-ttu-id="828bb-118">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="828bb-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="828bb-119">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="828bb-119">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="828bb-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="828bb-120">CommonParameters</span></span>
<span data-ttu-id="828bb-121">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="828bb-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="828bb-122">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="828bb-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="828bb-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="828bb-123">INPUTS</span></span>

### <span data-ttu-id="828bb-124">Keine</span><span class="sxs-lookup"><span data-stu-id="828bb-124">None</span></span>

## <span data-ttu-id="828bb-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="828bb-125">OUTPUTS</span></span>

### <span data-ttu-id="828bb-126">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span><span class="sxs-lookup"><span data-stu-id="828bb-126">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span></span>

## <span data-ttu-id="828bb-127">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="828bb-127">NOTES</span></span>

## <span data-ttu-id="828bb-128">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="828bb-128">RELATED LINKS</span></span>

[<span data-ttu-id="828bb-129">Remove-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="828bb-129">Remove-AzManagementPartner</span></span>](./Remove-AzManagementPartner.md)

[<span data-ttu-id="828bb-130">Get-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="828bb-130">Get-AzManagementPartner</span></span>](./Get-AzManagementPartner.md)

[<span data-ttu-id="828bb-131">Update-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="828bb-131">Update-AzManagementPartner</span></span>](./Update-AzManagementPartner.md)
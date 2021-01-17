---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagementPartner.dll-Help.xml
Module Name: Az.ManagementPartner
online version: https://docs.microsoft.com/en-us/powershell/module/az.managementpartner/update-azmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Update-AzManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Update-AzManagementPartner.md
ms.openlocfilehash: 326e16ff2f5bca8ca5ae987ebedf12cace87e11d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470423"
---
# <span data-ttu-id="1b1d1-101">Update-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="1b1d1-101">Update-AzManagementPartner</span></span>

## <span data-ttu-id="1b1d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b1d1-102">SYNOPSIS</span></span>
<span data-ttu-id="1b1d1-103">Aktualisiert die Microsoft Partner Network(MPN)-ID des aktuell authentifizierten Benutzers oder Dienstprinzipal.</span><span class="sxs-lookup"><span data-stu-id="1b1d1-103">Updates the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="1b1d1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1b1d1-104">SYNTAX</span></span>

```
Update-AzManagementPartner [-PartnerId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b1d1-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1b1d1-105">DESCRIPTION</span></span>
<span data-ttu-id="1b1d1-106">Aktualisiert die Microsoft Partner Network(MPN)-ID des aktuell authentifizierten Benutzers oder Dienstprinzipal.</span><span class="sxs-lookup"><span data-stu-id="1b1d1-106">Updates the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="1b1d1-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1b1d1-107">EXAMPLES</span></span>

### <span data-ttu-id="1b1d1-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1b1d1-108">Example 1</span></span>
```powershell
PS C:\> Update-AzManagementPartner -PartnerId 4977985
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="1b1d1-109">Aktualisieren des Managementpartners auf einen neuen Partner</span><span class="sxs-lookup"><span data-stu-id="1b1d1-109">Update the management partner to a new one</span></span>

## <span data-ttu-id="1b1d1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1b1d1-110">PARAMETERS</span></span>

### <span data-ttu-id="1b1d1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b1d1-111">-DefaultProfile</span></span>
<span data-ttu-id="1b1d1-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1b1d1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b1d1-113">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="1b1d1-113">-PartnerId</span></span>
<span data-ttu-id="1b1d1-114">Die 6-stellige Nummer des Managementpartners</span><span class="sxs-lookup"><span data-stu-id="1b1d1-114">The management partner id, it is a 6 digits number</span></span>

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

### <span data-ttu-id="1b1d1-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1b1d1-115">-Confirm</span></span>
<span data-ttu-id="1b1d1-116">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1b1d1-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b1d1-117">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="1b1d1-117">-WhatIf</span></span>
<span data-ttu-id="1b1d1-118">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1b1d1-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b1d1-119">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1b1d1-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b1d1-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b1d1-120">CommonParameters</span></span>
<span data-ttu-id="1b1d1-121">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b1d1-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b1d1-122">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b1d1-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b1d1-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1b1d1-123">INPUTS</span></span>

### <span data-ttu-id="1b1d1-124">Keine</span><span class="sxs-lookup"><span data-stu-id="1b1d1-124">None</span></span>

## <span data-ttu-id="1b1d1-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1b1d1-125">OUTPUTS</span></span>

### <span data-ttu-id="1b1d1-126">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span><span class="sxs-lookup"><span data-stu-id="1b1d1-126">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span></span>

## <span data-ttu-id="1b1d1-127">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1b1d1-127">NOTES</span></span>

## <span data-ttu-id="1b1d1-128">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1b1d1-128">RELATED LINKS</span></span>

[<span data-ttu-id="1b1d1-129">Remove-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="1b1d1-129">Remove-AzManagementPartner</span></span>](./Remove-AzManagementPartner.md)

[<span data-ttu-id="1b1d1-130">New-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="1b1d1-130">New-AzManagementPartner</span></span>](./New-AzManagementPartner.md)

[<span data-ttu-id="1b1d1-131">Get-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="1b1d1-131">Get-AzManagementPartner</span></span>](./Get-AzManagementPartner.md)
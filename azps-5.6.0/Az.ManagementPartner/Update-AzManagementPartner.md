---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagementPartner.dll-Help.xml
Module Name: Az.ManagementPartner
online version: https://docs.microsoft.com/powershell/module/az.managementpartner/update-azmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Update-AzManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Update-AzManagementPartner.md
ms.openlocfilehash: 493f4b3e1cfaa3be59d0bd402e2c0d13dfdfad4f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101946096"
---
# <span data-ttu-id="5c09b-101">Update-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="5c09b-101">Update-AzManagementPartner</span></span>

## <span data-ttu-id="5c09b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c09b-102">SYNOPSIS</span></span>
<span data-ttu-id="5c09b-103">Aktualisiert die Microsoft Partner Network(MPN)-ID des aktuell authentifizierten Benutzers oder Dienstprinzipals.</span><span class="sxs-lookup"><span data-stu-id="5c09b-103">Updates the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="5c09b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5c09b-104">SYNTAX</span></span>

```
Update-AzManagementPartner [-PartnerId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c09b-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5c09b-105">DESCRIPTION</span></span>
<span data-ttu-id="5c09b-106">Aktualisiert die Microsoft Partner Network(MPN)-ID des aktuell authentifizierten Benutzers oder Dienstprinzipals.</span><span class="sxs-lookup"><span data-stu-id="5c09b-106">Updates the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="5c09b-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5c09b-107">EXAMPLES</span></span>

### <span data-ttu-id="5c09b-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5c09b-108">Example 1</span></span>
```powershell
PS C:\> Update-AzManagementPartner -PartnerId 4977985
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="5c09b-109">Aktualisieren des Managementpartners auf einen neuen Partner</span><span class="sxs-lookup"><span data-stu-id="5c09b-109">Update the management partner to a new one</span></span>

## <span data-ttu-id="5c09b-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="5c09b-110">PARAMETERS</span></span>

### <span data-ttu-id="5c09b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c09b-111">-DefaultProfile</span></span>
<span data-ttu-id="5c09b-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5c09b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c09b-113">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="5c09b-113">-PartnerId</span></span>
<span data-ttu-id="5c09b-114">Die Id des Managementpartners ist eine 6-stellige Zahl.</span><span class="sxs-lookup"><span data-stu-id="5c09b-114">The management partner id, it is a 6 digits number</span></span>

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

### <span data-ttu-id="5c09b-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5c09b-115">-Confirm</span></span>
<span data-ttu-id="5c09b-116">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5c09b-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c09b-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c09b-117">-WhatIf</span></span>
<span data-ttu-id="5c09b-118">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5c09b-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c09b-119">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5c09b-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c09b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c09b-120">CommonParameters</span></span>
<span data-ttu-id="5c09b-121">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c09b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c09b-122">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c09b-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c09b-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5c09b-123">INPUTS</span></span>

### <span data-ttu-id="5c09b-124">Keine</span><span class="sxs-lookup"><span data-stu-id="5c09b-124">None</span></span>

## <span data-ttu-id="5c09b-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5c09b-125">OUTPUTS</span></span>

### <span data-ttu-id="5c09b-126">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span><span class="sxs-lookup"><span data-stu-id="5c09b-126">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span></span>

## <span data-ttu-id="5c09b-127">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="5c09b-127">NOTES</span></span>

## <span data-ttu-id="5c09b-128">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="5c09b-128">RELATED LINKS</span></span>

[<span data-ttu-id="5c09b-129">Remove-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="5c09b-129">Remove-AzManagementPartner</span></span>](./Remove-AzManagementPartner.md)

[<span data-ttu-id="5c09b-130">New-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="5c09b-130">New-AzManagementPartner</span></span>](./New-AzManagementPartner.md)

[<span data-ttu-id="5c09b-131">Get-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="5c09b-131">Get-AzManagementPartner</span></span>](./Get-AzManagementPartner.md)
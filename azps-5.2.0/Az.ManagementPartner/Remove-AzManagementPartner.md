---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagementPartner.dll-Help.xml
Module Name: Az.ManagementPartner
online version: https://docs.microsoft.com/en-us/powershell/module/az.managementpartner/remove-azmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Remove-AzManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Remove-AzManagementPartner.md
ms.openlocfilehash: db87797573d3f6c06b52aa072773c9af1a1be1fb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98292510"
---
# <span data-ttu-id="8cb06-101">Remove-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="8cb06-101">Remove-AzManagementPartner</span></span>

## <span data-ttu-id="8cb06-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8cb06-102">SYNOPSIS</span></span>
<span data-ttu-id="8cb06-103">Löschen Sie die MICROSOFT Partner Network(MPN)-ID des aktuell authentifizierten Benutzers oder Dienstprinzipal.</span><span class="sxs-lookup"><span data-stu-id="8cb06-103">Delete the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="8cb06-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8cb06-104">SYNTAX</span></span>

```
Remove-AzManagementPartner [-PartnerId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8cb06-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8cb06-105">DESCRIPTION</span></span>
<span data-ttu-id="8cb06-106">Löschen Sie die MICROSOFT Partner Network(MPN)-ID des aktuell authentifizierten Benutzers oder Dienstprinzipal.</span><span class="sxs-lookup"><span data-stu-id="8cb06-106">Delete the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="8cb06-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8cb06-107">EXAMPLES</span></span>

### <span data-ttu-id="8cb06-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8cb06-108">Example 1</span></span>
```powershell
PS C:\>Remove-AzManagementPartner -PartnerId 123457 -PassThru
true
```

<span data-ttu-id="8cb06-109">Managementpartner entfernen</span><span class="sxs-lookup"><span data-stu-id="8cb06-109">Remove management partner</span></span>

## <span data-ttu-id="8cb06-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8cb06-110">PARAMETERS</span></span>

### <span data-ttu-id="8cb06-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cb06-111">-DefaultProfile</span></span>
<span data-ttu-id="8cb06-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8cb06-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8cb06-113">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="8cb06-113">-PartnerId</span></span>
<span data-ttu-id="8cb06-114">Die 6-stellige Nummer des Managementpartners</span><span class="sxs-lookup"><span data-stu-id="8cb06-114">The management partner id, it is a 6 digits number</span></span>

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

### <span data-ttu-id="8cb06-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8cb06-115">-PassThru</span></span>
<span data-ttu-id="8cb06-116">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="8cb06-116">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cb06-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8cb06-117">-Confirm</span></span>
<span data-ttu-id="8cb06-118">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8cb06-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8cb06-119">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="8cb06-119">-WhatIf</span></span>
<span data-ttu-id="8cb06-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8cb06-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8cb06-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8cb06-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8cb06-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cb06-122">CommonParameters</span></span>
<span data-ttu-id="8cb06-123">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8cb06-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cb06-124">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8cb06-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cb06-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8cb06-125">INPUTS</span></span>

### <span data-ttu-id="8cb06-126">Keine</span><span class="sxs-lookup"><span data-stu-id="8cb06-126">None</span></span>

## <span data-ttu-id="8cb06-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8cb06-127">OUTPUTS</span></span>

### <span data-ttu-id="8cb06-128">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8cb06-128">System.Boolean</span></span>

## <span data-ttu-id="8cb06-129">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="8cb06-129">NOTES</span></span>

## <span data-ttu-id="8cb06-130">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="8cb06-130">RELATED LINKS</span></span>

[<span data-ttu-id="8cb06-131">New-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="8cb06-131">New-AzManagementPartner</span></span>](./New-AzManagementPartner.md)

[<span data-ttu-id="8cb06-132">Get-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="8cb06-132">Get-AzManagementPartner</span></span>](./Get-AzManagementPartner.md)

[<span data-ttu-id="8cb06-133">Update-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="8cb06-133">Update-AzManagementPartner</span></span>](./Update-AzManagementPartner.md)
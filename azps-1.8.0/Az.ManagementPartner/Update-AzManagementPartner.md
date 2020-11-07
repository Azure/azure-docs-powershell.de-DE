---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagementPartner.dll-Help.xml
Module Name: Az.ManagementPartner
online version: https://docs.microsoft.com/en-us/powershell/module/az.managementpartner/update-azmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Update-AzManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Update-AzManagementPartner.md
ms.openlocfilehash: 20d258cdd99da4e76fcf8394ebbe1aadd54f2fb1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93819111"
---
# <span data-ttu-id="6403d-101">Update-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="6403d-101">Update-AzManagementPartner</span></span>

## <span data-ttu-id="6403d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6403d-102">SYNOPSIS</span></span>
<span data-ttu-id="6403d-103">Aktualisiert die Microsoft Partner Network (MPN)-ID des aktuellen authentifizierten Benutzers oder Dienst Prinzipals.</span><span class="sxs-lookup"><span data-stu-id="6403d-103">Updates the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="6403d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6403d-104">SYNTAX</span></span>

```
Update-AzManagementPartner [-PartnerId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6403d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6403d-105">DESCRIPTION</span></span>
<span data-ttu-id="6403d-106">Aktualisiert die Microsoft Partner Network (MPN)-ID des aktuellen authentifizierten Benutzers oder Dienst Prinzipals.</span><span class="sxs-lookup"><span data-stu-id="6403d-106">Updates the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="6403d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6403d-107">EXAMPLES</span></span>

### <span data-ttu-id="6403d-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6403d-108">Example 1</span></span>
```powershell
PS C:\> Update-AzManagementPartner -PartnerId 4977985
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="6403d-109">Aktualisieren des Verwaltungs Partners auf eine neue Version</span><span class="sxs-lookup"><span data-stu-id="6403d-109">Update the management partner to a new one</span></span>

## <span data-ttu-id="6403d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="6403d-110">PARAMETERS</span></span>

### <span data-ttu-id="6403d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6403d-111">-DefaultProfile</span></span>
<span data-ttu-id="6403d-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6403d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6403d-113">-Partner-Nr</span><span class="sxs-lookup"><span data-stu-id="6403d-113">-PartnerId</span></span>
<span data-ttu-id="6403d-114">Die VERWALTUNGSPARTNER-ID ist eine sechsstellige Zahl</span><span class="sxs-lookup"><span data-stu-id="6403d-114">The management partner id, it is a 6 digits number</span></span>

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

### <span data-ttu-id="6403d-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6403d-115">-Confirm</span></span>
<span data-ttu-id="6403d-116">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6403d-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6403d-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6403d-117">-WhatIf</span></span>
<span data-ttu-id="6403d-118">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6403d-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6403d-119">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6403d-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6403d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6403d-120">CommonParameters</span></span>
<span data-ttu-id="6403d-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6403d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6403d-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6403d-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6403d-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6403d-123">INPUTS</span></span>

### <span data-ttu-id="6403d-124">Keine</span><span class="sxs-lookup"><span data-stu-id="6403d-124">None</span></span>

## <span data-ttu-id="6403d-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6403d-125">OUTPUTS</span></span>

### <span data-ttu-id="6403d-126">Microsoft. Azure. Commands. ManagementPartner. PSManagementPartner</span><span class="sxs-lookup"><span data-stu-id="6403d-126">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span></span>

## <span data-ttu-id="6403d-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="6403d-127">NOTES</span></span>

## <span data-ttu-id="6403d-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6403d-128">RELATED LINKS</span></span>

[<span data-ttu-id="6403d-129">Remove-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="6403d-129">Remove-AzManagementPartner</span></span>](./Remove-AzManagementPartner.md)

[<span data-ttu-id="6403d-130">Neu – AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="6403d-130">New-AzManagementPartner</span></span>](./New-AzManagementPartner.md)

[<span data-ttu-id="6403d-131">Get-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="6403d-131">Get-AzManagementPartner</span></span>](./Get-AzManagementPartner.md)
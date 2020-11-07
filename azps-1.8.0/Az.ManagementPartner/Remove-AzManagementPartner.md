---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagementPartner.dll-Help.xml
Module Name: Az.ManagementPartner
online version: https://docs.microsoft.com/en-us/powershell/module/az.managementpartner/remove-azmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Remove-AzManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Remove-AzManagementPartner.md
ms.openlocfilehash: 5910d82ddee49ba47c709a3323f72e325f4067ae
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93819112"
---
# <span data-ttu-id="5a85a-101">Remove-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="5a85a-101">Remove-AzManagementPartner</span></span>

## <span data-ttu-id="5a85a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5a85a-102">SYNOPSIS</span></span>
<span data-ttu-id="5a85a-103">Löschen Sie die Microsoft Partner Network (MPN)-ID des aktuellen authentifizierten Benutzers oder Dienst Prinzipals.</span><span class="sxs-lookup"><span data-stu-id="5a85a-103">Delete the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="5a85a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5a85a-104">SYNTAX</span></span>

```
Remove-AzManagementPartner [-PartnerId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a85a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5a85a-105">DESCRIPTION</span></span>
<span data-ttu-id="5a85a-106">Löschen Sie die Microsoft Partner Network (MPN)-ID des aktuellen authentifizierten Benutzers oder Dienst Prinzipals.</span><span class="sxs-lookup"><span data-stu-id="5a85a-106">Delete the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="5a85a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5a85a-107">EXAMPLES</span></span>

### <span data-ttu-id="5a85a-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5a85a-108">Example 1</span></span>
```powershell
PS C:\>Remove-AzManagementPartner -PartnerId 123457 -PassThru
true
```

<span data-ttu-id="5a85a-109">VERWALTUNGSPARTNER entfernen</span><span class="sxs-lookup"><span data-stu-id="5a85a-109">Remove management partner</span></span>

## <span data-ttu-id="5a85a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="5a85a-110">PARAMETERS</span></span>

### <span data-ttu-id="5a85a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a85a-111">-DefaultProfile</span></span>
<span data-ttu-id="5a85a-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5a85a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a85a-113">-Partner-Nr</span><span class="sxs-lookup"><span data-stu-id="5a85a-113">-PartnerId</span></span>
<span data-ttu-id="5a85a-114">Die VERWALTUNGSPARTNER-ID ist eine sechsstellige Zahl</span><span class="sxs-lookup"><span data-stu-id="5a85a-114">The management partner id, it is a 6 digits number</span></span>

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

### <span data-ttu-id="5a85a-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5a85a-115">-PassThru</span></span>
<span data-ttu-id="5a85a-116">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="5a85a-116">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="5a85a-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5a85a-117">-Confirm</span></span>
<span data-ttu-id="5a85a-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5a85a-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a85a-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a85a-119">-WhatIf</span></span>
<span data-ttu-id="5a85a-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5a85a-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a85a-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5a85a-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a85a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a85a-122">CommonParameters</span></span>
<span data-ttu-id="5a85a-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a85a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a85a-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a85a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a85a-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5a85a-125">INPUTS</span></span>

### <span data-ttu-id="5a85a-126">Keine</span><span class="sxs-lookup"><span data-stu-id="5a85a-126">None</span></span>

## <span data-ttu-id="5a85a-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5a85a-127">OUTPUTS</span></span>

### <span data-ttu-id="5a85a-128">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5a85a-128">System.Boolean</span></span>

## <span data-ttu-id="5a85a-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="5a85a-129">NOTES</span></span>

## <span data-ttu-id="5a85a-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5a85a-130">RELATED LINKS</span></span>

[<span data-ttu-id="5a85a-131">Neu – AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="5a85a-131">New-AzManagementPartner</span></span>](./New-AzManagementPartner.md)

[<span data-ttu-id="5a85a-132">Get-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="5a85a-132">Get-AzManagementPartner</span></span>](./Get-AzManagementPartner.md)

[<span data-ttu-id="5a85a-133">Update-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="5a85a-133">Update-AzManagementPartner</span></span>](./Update-AzManagementPartner.md)
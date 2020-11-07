---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagementPartner.dll-Help.xml
Module Name: Az.ManagementPartner
online version: https://docs.microsoft.com/en-us/powershell/module/az.managementpartner/remove-azmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Remove-AzManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Remove-AzManagementPartner.md
ms.openlocfilehash: db87797573d3f6c06b52aa072773c9af1a1be1fb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845468"
---
# <span data-ttu-id="b1b8c-101">Remove-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="b1b8c-101">Remove-AzManagementPartner</span></span>

## <span data-ttu-id="b1b8c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b1b8c-102">SYNOPSIS</span></span>
<span data-ttu-id="b1b8c-103">Löschen Sie die Microsoft Partner Network (MPN)-ID des aktuellen authentifizierten Benutzers oder Dienst Prinzipals.</span><span class="sxs-lookup"><span data-stu-id="b1b8c-103">Delete the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="b1b8c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b1b8c-104">SYNTAX</span></span>

```
Remove-AzManagementPartner [-PartnerId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1b8c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b1b8c-105">DESCRIPTION</span></span>
<span data-ttu-id="b1b8c-106">Löschen Sie die Microsoft Partner Network (MPN)-ID des aktuellen authentifizierten Benutzers oder Dienst Prinzipals.</span><span class="sxs-lookup"><span data-stu-id="b1b8c-106">Delete the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="b1b8c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b1b8c-107">EXAMPLES</span></span>

### <span data-ttu-id="b1b8c-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b1b8c-108">Example 1</span></span>
```powershell
PS C:\>Remove-AzManagementPartner -PartnerId 123457 -PassThru
true
```

<span data-ttu-id="b1b8c-109">VERWALTUNGSPARTNER entfernen</span><span class="sxs-lookup"><span data-stu-id="b1b8c-109">Remove management partner</span></span>

## <span data-ttu-id="b1b8c-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="b1b8c-110">PARAMETERS</span></span>

### <span data-ttu-id="b1b8c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1b8c-111">-DefaultProfile</span></span>
<span data-ttu-id="b1b8c-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b1b8c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1b8c-113">-Partner-Nr</span><span class="sxs-lookup"><span data-stu-id="b1b8c-113">-PartnerId</span></span>
<span data-ttu-id="b1b8c-114">Die VERWALTUNGSPARTNER-ID ist eine sechsstellige Zahl</span><span class="sxs-lookup"><span data-stu-id="b1b8c-114">The management partner id, it is a 6 digits number</span></span>

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

### <span data-ttu-id="b1b8c-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b1b8c-115">-PassThru</span></span>
<span data-ttu-id="b1b8c-116">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="b1b8c-116">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="b1b8c-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b1b8c-117">-Confirm</span></span>
<span data-ttu-id="b1b8c-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b1b8c-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1b8c-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1b8c-119">-WhatIf</span></span>
<span data-ttu-id="b1b8c-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b1b8c-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1b8c-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b1b8c-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1b8c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1b8c-122">CommonParameters</span></span>
<span data-ttu-id="b1b8c-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1b8c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1b8c-124">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1b8c-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1b8c-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b1b8c-125">INPUTS</span></span>

### <span data-ttu-id="b1b8c-126">Keine</span><span class="sxs-lookup"><span data-stu-id="b1b8c-126">None</span></span>

## <span data-ttu-id="b1b8c-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b1b8c-127">OUTPUTS</span></span>

### <span data-ttu-id="b1b8c-128">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b1b8c-128">System.Boolean</span></span>

## <span data-ttu-id="b1b8c-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="b1b8c-129">NOTES</span></span>

## <span data-ttu-id="b1b8c-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b1b8c-130">RELATED LINKS</span></span>

[<span data-ttu-id="b1b8c-131">Neu – AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="b1b8c-131">New-AzManagementPartner</span></span>](./New-AzManagementPartner.md)

[<span data-ttu-id="b1b8c-132">Get-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="b1b8c-132">Get-AzManagementPartner</span></span>](./Get-AzManagementPartner.md)

[<span data-ttu-id="b1b8c-133">Update-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="b1b8c-133">Update-AzManagementPartner</span></span>](./Update-AzManagementPartner.md)
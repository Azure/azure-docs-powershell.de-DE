---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzSecurityContact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityContact.md
ms.openlocfilehash: b4cbecd2e29a0b70c7e62194df2364b22b33b462
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100174196"
---
# <span data-ttu-id="262da-101">Remove-AzSecurityContact</span><span class="sxs-lookup"><span data-stu-id="262da-101">Remove-AzSecurityContact</span></span>

## <span data-ttu-id="262da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="262da-102">SYNOPSIS</span></span>
<span data-ttu-id="262da-103">Löscht einen Sicherheitskontakt.</span><span class="sxs-lookup"><span data-stu-id="262da-103">Deletes a security contact.</span></span>

## <span data-ttu-id="262da-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="262da-104">SYNTAX</span></span>

### <span data-ttu-id="262da-105">SubscriptionLevelResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="262da-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzSecurityContact -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="262da-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="262da-106">ResourceId</span></span>
```
Remove-AzSecurityContact -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="262da-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="262da-107">InputObject</span></span>
```
Remove-AzSecurityContact -InputObject <PSSecurityContact> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="262da-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="262da-108">DESCRIPTION</span></span>
<span data-ttu-id="262da-109">Löscht einen Sicherheitskontakt.</span><span class="sxs-lookup"><span data-stu-id="262da-109">Deletes a security contact.</span></span>

## <span data-ttu-id="262da-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="262da-110">EXAMPLES</span></span>

### <span data-ttu-id="262da-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="262da-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSecurityContact -Name "default1"
```

<span data-ttu-id="262da-112">Löscht den Sicherheitskontakt "default1".</span><span class="sxs-lookup"><span data-stu-id="262da-112">Deletes the "default1" security contact</span></span>

## <span data-ttu-id="262da-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="262da-113">PARAMETERS</span></span>

### <span data-ttu-id="262da-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="262da-114">-DefaultProfile</span></span>
<span data-ttu-id="262da-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="262da-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="262da-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="262da-116">-InputObject</span></span>
<span data-ttu-id="262da-117">Eingabeobjekt.</span><span class="sxs-lookup"><span data-stu-id="262da-117">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="262da-118">-Name</span><span class="sxs-lookup"><span data-stu-id="262da-118">-Name</span></span>
<span data-ttu-id="262da-119">Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="262da-119">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="262da-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="262da-120">-PassThru</span></span>
<span data-ttu-id="262da-121">Gibt zurück, ob der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="262da-121">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="262da-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="262da-122">-ResourceId</span></span>
<span data-ttu-id="262da-123">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="262da-123">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="262da-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="262da-124">-Confirm</span></span>
<span data-ttu-id="262da-125">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="262da-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="262da-126">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="262da-126">-WhatIf</span></span>
<span data-ttu-id="262da-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="262da-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="262da-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="262da-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="262da-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="262da-129">CommonParameters</span></span>
<span data-ttu-id="262da-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="262da-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="262da-131">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="262da-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="262da-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="262da-132">INPUTS</span></span>

### <span data-ttu-id="262da-133">System.String</span><span class="sxs-lookup"><span data-stu-id="262da-133">System.String</span></span>

### <span data-ttu-id="262da-134">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span><span class="sxs-lookup"><span data-stu-id="262da-134">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span></span>

## <span data-ttu-id="262da-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="262da-135">OUTPUTS</span></span>

### <span data-ttu-id="262da-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="262da-136">System.Boolean</span></span>

## <span data-ttu-id="262da-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="262da-137">NOTES</span></span>

## <span data-ttu-id="262da-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="262da-138">RELATED LINKS</span></span>

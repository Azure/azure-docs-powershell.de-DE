---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Remove-AzSecurityContact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityContact.md
ms.openlocfilehash: f8b96d8441e9a0b3a5f9b9bc3c775da7d71f12c8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939400"
---
# <span data-ttu-id="8cba5-101">Remove-AzSecurityContact</span><span class="sxs-lookup"><span data-stu-id="8cba5-101">Remove-AzSecurityContact</span></span>

## <span data-ttu-id="8cba5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8cba5-102">SYNOPSIS</span></span>
<span data-ttu-id="8cba5-103">Löscht einen Sicherheitskontakt.</span><span class="sxs-lookup"><span data-stu-id="8cba5-103">Deletes a security contact.</span></span>

## <span data-ttu-id="8cba5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8cba5-104">SYNTAX</span></span>

### <span data-ttu-id="8cba5-105">SubscriptionLevelResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="8cba5-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzSecurityContact -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8cba5-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="8cba5-106">ResourceId</span></span>
```
Remove-AzSecurityContact -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8cba5-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="8cba5-107">InputObject</span></span>
```
Remove-AzSecurityContact -InputObject <PSSecurityContact> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8cba5-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8cba5-108">DESCRIPTION</span></span>
<span data-ttu-id="8cba5-109">Löscht einen Sicherheitskontakt.</span><span class="sxs-lookup"><span data-stu-id="8cba5-109">Deletes a security contact.</span></span>

## <span data-ttu-id="8cba5-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8cba5-110">EXAMPLES</span></span>

### <span data-ttu-id="8cba5-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8cba5-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSecurityContact -Name "default1"
```

<span data-ttu-id="8cba5-112">Löscht den Sicherheitskontakt "standard1".</span><span class="sxs-lookup"><span data-stu-id="8cba5-112">Deletes the "default1" security contact</span></span>

## <span data-ttu-id="8cba5-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="8cba5-113">PARAMETERS</span></span>

### <span data-ttu-id="8cba5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cba5-114">-DefaultProfile</span></span>
<span data-ttu-id="8cba5-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8cba5-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8cba5-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8cba5-116">-InputObject</span></span>
<span data-ttu-id="8cba5-117">Eingabeobjekt.</span><span class="sxs-lookup"><span data-stu-id="8cba5-117">Input Object.</span></span>

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

### <span data-ttu-id="8cba5-118">-Name</span><span class="sxs-lookup"><span data-stu-id="8cba5-118">-Name</span></span>
<span data-ttu-id="8cba5-119">Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="8cba5-119">Resource name.</span></span>

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

### <span data-ttu-id="8cba5-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8cba5-120">-PassThru</span></span>
<span data-ttu-id="8cba5-121">Gibt zurück, ob der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="8cba5-121">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="8cba5-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8cba5-122">-ResourceId</span></span>
<span data-ttu-id="8cba5-123">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="8cba5-123">Resource ID.</span></span>

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

### <span data-ttu-id="8cba5-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8cba5-124">-Confirm</span></span>
<span data-ttu-id="8cba5-125">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8cba5-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8cba5-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8cba5-126">-WhatIf</span></span>
<span data-ttu-id="8cba5-127">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8cba5-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8cba5-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8cba5-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8cba5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cba5-129">CommonParameters</span></span>
<span data-ttu-id="8cba5-130">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8cba5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cba5-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8cba5-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cba5-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8cba5-132">INPUTS</span></span>

### <span data-ttu-id="8cba5-133">System.String</span><span class="sxs-lookup"><span data-stu-id="8cba5-133">System.String</span></span>

### <span data-ttu-id="8cba5-134">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span><span class="sxs-lookup"><span data-stu-id="8cba5-134">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span></span>

## <span data-ttu-id="8cba5-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8cba5-135">OUTPUTS</span></span>

### <span data-ttu-id="8cba5-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8cba5-136">System.Boolean</span></span>

## <span data-ttu-id="8cba5-137">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="8cba5-137">NOTES</span></span>

## <span data-ttu-id="8cba5-138">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="8cba5-138">RELATED LINKS</span></span>

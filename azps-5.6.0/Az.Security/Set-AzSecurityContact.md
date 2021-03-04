---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Set-AzSecurityContact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityContact.md
ms.openlocfilehash: 8cd5adee5e8b992cf709b76996a70760f3fd90a5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936024"
---
# <span data-ttu-id="980fb-101">Set-AzSecurityContact</span><span class="sxs-lookup"><span data-stu-id="980fb-101">Set-AzSecurityContact</span></span>

## <span data-ttu-id="980fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="980fb-102">SYNOPSIS</span></span>
<span data-ttu-id="980fb-103">Aktualisiert einen Sicherheitskontakt für ein Abonnement.</span><span class="sxs-lookup"><span data-stu-id="980fb-103">Updates a security contact for a subscription.</span></span>

## <span data-ttu-id="980fb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="980fb-104">SYNTAX</span></span>

```
Set-AzSecurityContact -Name <String> -Email <String> [-Phone <String>] [-AlertAdmin] [-NotifyOnAlert]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="980fb-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="980fb-105">DESCRIPTION</span></span>
<span data-ttu-id="980fb-106">Aktualisiert einen Sicherheitskontakt für ein Abonnement.</span><span class="sxs-lookup"><span data-stu-id="980fb-106">Updates a security contact for a subscription.</span></span>

## <span data-ttu-id="980fb-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="980fb-107">EXAMPLES</span></span>

### <span data-ttu-id="980fb-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="980fb-108">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityContact -Name "default1" -Email "john@contoso.com" -Phone "214275-4038" -AlertAdmin -NotifyOnAlert

Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/securityContacts/
                     default1
Name               : default1
Email              : john@contoso.com
Phone              : 214275-4038
AlertNotifications : On
AlertsToAdmins     : On
```

<span data-ttu-id="980fb-109">Aktualisiert einen Sicherheitskontakt für ein Abonnement.</span><span class="sxs-lookup"><span data-stu-id="980fb-109">Updates a security contact for a subscription.</span></span>

## <span data-ttu-id="980fb-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="980fb-110">PARAMETERS</span></span>

### <span data-ttu-id="980fb-111">-AlertAdmin</span><span class="sxs-lookup"><span data-stu-id="980fb-111">-AlertAdmin</span></span>
<span data-ttu-id="980fb-112">Benachrichtigungen an Administratoren.</span><span class="sxs-lookup"><span data-stu-id="980fb-112">Alerts To Administrators.</span></span>

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

### <span data-ttu-id="980fb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="980fb-113">-DefaultProfile</span></span>
<span data-ttu-id="980fb-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="980fb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="980fb-115">-E-Mail</span><span class="sxs-lookup"><span data-stu-id="980fb-115">-Email</span></span>
<span data-ttu-id="980fb-116">E-Mail.</span><span class="sxs-lookup"><span data-stu-id="980fb-116">E-Mail.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="980fb-117">-Name</span><span class="sxs-lookup"><span data-stu-id="980fb-117">-Name</span></span>
<span data-ttu-id="980fb-118">Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="980fb-118">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="980fb-119">-NotifyOnAlert</span><span class="sxs-lookup"><span data-stu-id="980fb-119">-NotifyOnAlert</span></span>
<span data-ttu-id="980fb-120">Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="980fb-120">Alert Notifications.</span></span>

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

### <span data-ttu-id="980fb-121">-Phone</span><span class="sxs-lookup"><span data-stu-id="980fb-121">-Phone</span></span>
<span data-ttu-id="980fb-122">Telefon.</span><span class="sxs-lookup"><span data-stu-id="980fb-122">Phone.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="980fb-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="980fb-123">-Confirm</span></span>
<span data-ttu-id="980fb-124">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="980fb-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="980fb-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="980fb-125">-WhatIf</span></span>
<span data-ttu-id="980fb-126">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="980fb-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="980fb-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="980fb-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="980fb-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="980fb-128">CommonParameters</span></span>
<span data-ttu-id="980fb-129">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="980fb-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="980fb-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="980fb-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="980fb-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="980fb-131">INPUTS</span></span>

### <span data-ttu-id="980fb-132">Keine</span><span class="sxs-lookup"><span data-stu-id="980fb-132">None</span></span>

## <span data-ttu-id="980fb-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="980fb-133">OUTPUTS</span></span>

### <span data-ttu-id="980fb-134">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span><span class="sxs-lookup"><span data-stu-id="980fb-134">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span></span>

## <span data-ttu-id="980fb-135">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="980fb-135">NOTES</span></span>

## <span data-ttu-id="980fb-136">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="980fb-136">RELATED LINKS</span></span>

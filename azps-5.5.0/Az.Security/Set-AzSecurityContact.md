---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityContact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityContact.md
ms.openlocfilehash: 504f07092a0a8e246e778421748f1cd807b04a77
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100174140"
---
# <span data-ttu-id="82706-101">Set-AzSecurityContact</span><span class="sxs-lookup"><span data-stu-id="82706-101">Set-AzSecurityContact</span></span>

## <span data-ttu-id="82706-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82706-102">SYNOPSIS</span></span>
<span data-ttu-id="82706-103">Aktualisiert einen Sicherheitskontakt für ein Abonnement.</span><span class="sxs-lookup"><span data-stu-id="82706-103">Updates a security contact for a subscription.</span></span>

## <span data-ttu-id="82706-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="82706-104">SYNTAX</span></span>

```
Set-AzSecurityContact -Name <String> -Email <String> [-Phone <String>] [-AlertAdmin] [-NotifyOnAlert]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82706-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="82706-105">DESCRIPTION</span></span>
<span data-ttu-id="82706-106">Aktualisiert einen Sicherheitskontakt für ein Abonnement.</span><span class="sxs-lookup"><span data-stu-id="82706-106">Updates a security contact for a subscription.</span></span>

## <span data-ttu-id="82706-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="82706-107">EXAMPLES</span></span>

### <span data-ttu-id="82706-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="82706-108">Example 1</span></span>
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

<span data-ttu-id="82706-109">Aktualisiert einen Sicherheitskontakt für ein Abonnement.</span><span class="sxs-lookup"><span data-stu-id="82706-109">Updates a security contact for a subscription.</span></span>

## <span data-ttu-id="82706-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="82706-110">PARAMETERS</span></span>

### <span data-ttu-id="82706-111">-AlertAdmin</span><span class="sxs-lookup"><span data-stu-id="82706-111">-AlertAdmin</span></span>
<span data-ttu-id="82706-112">Benachrichtigungen für Administratoren.</span><span class="sxs-lookup"><span data-stu-id="82706-112">Alerts To Administrators.</span></span>

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

### <span data-ttu-id="82706-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82706-113">-DefaultProfile</span></span>
<span data-ttu-id="82706-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="82706-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82706-115">-Email</span><span class="sxs-lookup"><span data-stu-id="82706-115">-Email</span></span>
<span data-ttu-id="82706-116">"E-Mail" aus.</span><span class="sxs-lookup"><span data-stu-id="82706-116">E-Mail.</span></span>

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

### <span data-ttu-id="82706-117">-Name</span><span class="sxs-lookup"><span data-stu-id="82706-117">-Name</span></span>
<span data-ttu-id="82706-118">Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="82706-118">Resource name.</span></span>

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

### <span data-ttu-id="82706-119">-NotifyOnAlert</span><span class="sxs-lookup"><span data-stu-id="82706-119">-NotifyOnAlert</span></span>
<span data-ttu-id="82706-120">"Benachrichtigungen" aus.</span><span class="sxs-lookup"><span data-stu-id="82706-120">Alert Notifications.</span></span>

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

### <span data-ttu-id="82706-121">-Phone</span><span class="sxs-lookup"><span data-stu-id="82706-121">-Phone</span></span>
<span data-ttu-id="82706-122">"Telefon" aus.</span><span class="sxs-lookup"><span data-stu-id="82706-122">Phone.</span></span>

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

### <span data-ttu-id="82706-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="82706-123">-Confirm</span></span>
<span data-ttu-id="82706-124">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="82706-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82706-125">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="82706-125">-WhatIf</span></span>
<span data-ttu-id="82706-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="82706-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="82706-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="82706-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82706-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82706-128">CommonParameters</span></span>
<span data-ttu-id="82706-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82706-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82706-130">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="82706-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82706-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="82706-131">INPUTS</span></span>

### <span data-ttu-id="82706-132">Keine</span><span class="sxs-lookup"><span data-stu-id="82706-132">None</span></span>

## <span data-ttu-id="82706-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="82706-133">OUTPUTS</span></span>

### <span data-ttu-id="82706-134">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span><span class="sxs-lookup"><span data-stu-id="82706-134">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span></span>

## <span data-ttu-id="82706-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="82706-135">NOTES</span></span>

## <span data-ttu-id="82706-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="82706-136">RELATED LINKS</span></span>

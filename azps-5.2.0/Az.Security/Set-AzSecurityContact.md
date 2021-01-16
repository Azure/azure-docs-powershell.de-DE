---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityContact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityContact.md
ms.openlocfilehash: 504f07092a0a8e246e778421748f1cd807b04a77
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98308699"
---
# <span data-ttu-id="94194-101">Set-AzSecurityContact</span><span class="sxs-lookup"><span data-stu-id="94194-101">Set-AzSecurityContact</span></span>

## <span data-ttu-id="94194-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94194-102">SYNOPSIS</span></span>
<span data-ttu-id="94194-103">Aktualisiert einen Sicherheitskontakt für ein Abonnement.</span><span class="sxs-lookup"><span data-stu-id="94194-103">Updates a security contact for a subscription.</span></span>

## <span data-ttu-id="94194-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="94194-104">SYNTAX</span></span>

```
Set-AzSecurityContact -Name <String> -Email <String> [-Phone <String>] [-AlertAdmin] [-NotifyOnAlert]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94194-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="94194-105">DESCRIPTION</span></span>
<span data-ttu-id="94194-106">Aktualisiert einen Sicherheitskontakt für ein Abonnement.</span><span class="sxs-lookup"><span data-stu-id="94194-106">Updates a security contact for a subscription.</span></span>

## <span data-ttu-id="94194-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="94194-107">EXAMPLES</span></span>

### <span data-ttu-id="94194-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="94194-108">Example 1</span></span>
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

<span data-ttu-id="94194-109">Aktualisiert einen Sicherheitskontakt für ein Abonnement.</span><span class="sxs-lookup"><span data-stu-id="94194-109">Updates a security contact for a subscription.</span></span>

## <span data-ttu-id="94194-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="94194-110">PARAMETERS</span></span>

### <span data-ttu-id="94194-111">-AlertAdmin</span><span class="sxs-lookup"><span data-stu-id="94194-111">-AlertAdmin</span></span>
<span data-ttu-id="94194-112">Benachrichtigungen für Administratoren.</span><span class="sxs-lookup"><span data-stu-id="94194-112">Alerts To Administrators.</span></span>

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

### <span data-ttu-id="94194-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94194-113">-DefaultProfile</span></span>
<span data-ttu-id="94194-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="94194-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94194-115">-E-Mail</span><span class="sxs-lookup"><span data-stu-id="94194-115">-Email</span></span>
<span data-ttu-id="94194-116">"E-Mail" aus.</span><span class="sxs-lookup"><span data-stu-id="94194-116">E-Mail.</span></span>

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

### <span data-ttu-id="94194-117">-Name</span><span class="sxs-lookup"><span data-stu-id="94194-117">-Name</span></span>
<span data-ttu-id="94194-118">Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="94194-118">Resource name.</span></span>

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

### <span data-ttu-id="94194-119">-NotifyOnAlert</span><span class="sxs-lookup"><span data-stu-id="94194-119">-NotifyOnAlert</span></span>
<span data-ttu-id="94194-120">"Benachrichtigungen" aus.</span><span class="sxs-lookup"><span data-stu-id="94194-120">Alert Notifications.</span></span>

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

### <span data-ttu-id="94194-121">-Phone</span><span class="sxs-lookup"><span data-stu-id="94194-121">-Phone</span></span>
<span data-ttu-id="94194-122">"Telefon" aus.</span><span class="sxs-lookup"><span data-stu-id="94194-122">Phone.</span></span>

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

### <span data-ttu-id="94194-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="94194-123">-Confirm</span></span>
<span data-ttu-id="94194-124">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="94194-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94194-125">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="94194-125">-WhatIf</span></span>
<span data-ttu-id="94194-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="94194-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="94194-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="94194-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94194-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94194-128">CommonParameters</span></span>
<span data-ttu-id="94194-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94194-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94194-130">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="94194-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94194-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="94194-131">INPUTS</span></span>

### <span data-ttu-id="94194-132">Keine</span><span class="sxs-lookup"><span data-stu-id="94194-132">None</span></span>

## <span data-ttu-id="94194-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="94194-133">OUTPUTS</span></span>

### <span data-ttu-id="94194-134">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span><span class="sxs-lookup"><span data-stu-id="94194-134">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span></span>

## <span data-ttu-id="94194-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="94194-135">NOTES</span></span>

## <span data-ttu-id="94194-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="94194-136">RELATED LINKS</span></span>

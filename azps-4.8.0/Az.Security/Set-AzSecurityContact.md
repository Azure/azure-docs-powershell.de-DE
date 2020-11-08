---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityContact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityContact.md
ms.openlocfilehash: 504f07092a0a8e246e778421748f1cd807b04a77
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165582"
---
# <span data-ttu-id="cf79c-101">Set-AzSecurityContact</span><span class="sxs-lookup"><span data-stu-id="cf79c-101">Set-AzSecurityContact</span></span>

## <span data-ttu-id="cf79c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cf79c-102">SYNOPSIS</span></span>
<span data-ttu-id="cf79c-103">Aktualisiert einen Sicherheitskontakt für ein Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cf79c-103">Updates a security contact for a subscription.</span></span>

## <span data-ttu-id="cf79c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cf79c-104">SYNTAX</span></span>

```
Set-AzSecurityContact -Name <String> -Email <String> [-Phone <String>] [-AlertAdmin] [-NotifyOnAlert]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf79c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cf79c-105">DESCRIPTION</span></span>
<span data-ttu-id="cf79c-106">Aktualisiert einen Sicherheitskontakt für ein Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cf79c-106">Updates a security contact for a subscription.</span></span>

## <span data-ttu-id="cf79c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cf79c-107">EXAMPLES</span></span>

### <span data-ttu-id="cf79c-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="cf79c-108">Example 1</span></span>
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

<span data-ttu-id="cf79c-109">Aktualisiert einen Sicherheitskontakt für ein Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cf79c-109">Updates a security contact for a subscription.</span></span>

## <span data-ttu-id="cf79c-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="cf79c-110">PARAMETERS</span></span>

### <span data-ttu-id="cf79c-111">-AlertAdmin</span><span class="sxs-lookup"><span data-stu-id="cf79c-111">-AlertAdmin</span></span>
<span data-ttu-id="cf79c-112">Benachrichtigungen an Administratoren.</span><span class="sxs-lookup"><span data-stu-id="cf79c-112">Alerts To Administrators.</span></span>

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

### <span data-ttu-id="cf79c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf79c-113">-DefaultProfile</span></span>
<span data-ttu-id="cf79c-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cf79c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf79c-115">– E-Mail</span><span class="sxs-lookup"><span data-stu-id="cf79c-115">-Email</span></span>
<span data-ttu-id="cf79c-116">E-Mail.</span><span class="sxs-lookup"><span data-stu-id="cf79c-116">E-Mail.</span></span>

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

### <span data-ttu-id="cf79c-117">-Name</span><span class="sxs-lookup"><span data-stu-id="cf79c-117">-Name</span></span>
<span data-ttu-id="cf79c-118">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="cf79c-118">Resource name.</span></span>

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

### <span data-ttu-id="cf79c-119">-NotifyOnAlert</span><span class="sxs-lookup"><span data-stu-id="cf79c-119">-NotifyOnAlert</span></span>
<span data-ttu-id="cf79c-120">Benachrichtigungs Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="cf79c-120">Alert Notifications.</span></span>

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

### <span data-ttu-id="cf79c-121">-Telefon</span><span class="sxs-lookup"><span data-stu-id="cf79c-121">-Phone</span></span>
<span data-ttu-id="cf79c-122">Telefon.</span><span class="sxs-lookup"><span data-stu-id="cf79c-122">Phone.</span></span>

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

### <span data-ttu-id="cf79c-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="cf79c-123">-Confirm</span></span>
<span data-ttu-id="cf79c-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cf79c-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf79c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf79c-125">-WhatIf</span></span>
<span data-ttu-id="cf79c-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cf79c-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cf79c-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cf79c-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf79c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf79c-128">CommonParameters</span></span>
<span data-ttu-id="cf79c-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf79c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf79c-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cf79c-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf79c-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cf79c-131">INPUTS</span></span>

### <span data-ttu-id="cf79c-132">Keine</span><span class="sxs-lookup"><span data-stu-id="cf79c-132">None</span></span>

## <span data-ttu-id="cf79c-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cf79c-133">OUTPUTS</span></span>

### <span data-ttu-id="cf79c-134">Microsoft. Azure. Commands. Security. Models. SecurityContacts. PSSecurityContact</span><span class="sxs-lookup"><span data-stu-id="cf79c-134">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span></span>

## <span data-ttu-id="cf79c-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="cf79c-135">NOTES</span></span>

## <span data-ttu-id="cf79c-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cf79c-136">RELATED LINKS</span></span>

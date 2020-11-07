---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityContact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityContact.md
ms.openlocfilehash: 1bf9e6b51899054899e819784872cf688a182e16
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659430"
---
# <span data-ttu-id="e097e-101">Set-AzSecurityContact</span><span class="sxs-lookup"><span data-stu-id="e097e-101">Set-AzSecurityContact</span></span>

## <span data-ttu-id="e097e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e097e-102">SYNOPSIS</span></span>
<span data-ttu-id="e097e-103">Aktualisiert einen Sicherheitskontakt für ein Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e097e-103">Updates a security contact for a subscription.</span></span>

## <span data-ttu-id="e097e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e097e-104">SYNTAX</span></span>

```
Set-AzSecurityContact -Name <String> -Email <String> [-Phone <String>] [-AlertAdmin] [-NotifyOnAlert]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e097e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e097e-105">DESCRIPTION</span></span>
<span data-ttu-id="e097e-106">Aktualisiert einen Sicherheitskontakt für ein Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e097e-106">Updates a security contact for a subscription.</span></span>

## <span data-ttu-id="e097e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e097e-107">EXAMPLES</span></span>

### <span data-ttu-id="e097e-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e097e-108">Example 1</span></span>
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

<span data-ttu-id="e097e-109">Aktualisiert einen Sicherheitskontakt für ein Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e097e-109">Updates a security contact for a subscription.</span></span>

## <span data-ttu-id="e097e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e097e-110">PARAMETERS</span></span>

### <span data-ttu-id="e097e-111">-AlertAdmin</span><span class="sxs-lookup"><span data-stu-id="e097e-111">-AlertAdmin</span></span>
<span data-ttu-id="e097e-112">Benachrichtigungen an Administratoren.</span><span class="sxs-lookup"><span data-stu-id="e097e-112">Alerts To Administrators.</span></span>

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

### <span data-ttu-id="e097e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e097e-113">-DefaultProfile</span></span>
<span data-ttu-id="e097e-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e097e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e097e-115">– E-Mail</span><span class="sxs-lookup"><span data-stu-id="e097e-115">-Email</span></span>
<span data-ttu-id="e097e-116">E-Mail.</span><span class="sxs-lookup"><span data-stu-id="e097e-116">E-Mail.</span></span>

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

### <span data-ttu-id="e097e-117">-Name</span><span class="sxs-lookup"><span data-stu-id="e097e-117">-Name</span></span>
<span data-ttu-id="e097e-118">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="e097e-118">Resource name.</span></span>

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

### <span data-ttu-id="e097e-119">-NotifyOnAlert</span><span class="sxs-lookup"><span data-stu-id="e097e-119">-NotifyOnAlert</span></span>
<span data-ttu-id="e097e-120">Benachrichtigungs Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="e097e-120">Alert Notifications.</span></span>

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

### <span data-ttu-id="e097e-121">-Telefon</span><span class="sxs-lookup"><span data-stu-id="e097e-121">-Phone</span></span>
<span data-ttu-id="e097e-122">Telefon.</span><span class="sxs-lookup"><span data-stu-id="e097e-122">Phone.</span></span>

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

### <span data-ttu-id="e097e-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e097e-123">-Confirm</span></span>
<span data-ttu-id="e097e-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e097e-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e097e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e097e-125">-WhatIf</span></span>
<span data-ttu-id="e097e-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e097e-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e097e-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e097e-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e097e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e097e-128">CommonParameters</span></span>
<span data-ttu-id="e097e-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e097e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e097e-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e097e-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e097e-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e097e-131">INPUTS</span></span>

### <span data-ttu-id="e097e-132">Keine</span><span class="sxs-lookup"><span data-stu-id="e097e-132">None</span></span>

## <span data-ttu-id="e097e-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e097e-133">OUTPUTS</span></span>

### <span data-ttu-id="e097e-134">Microsoft. Azure. Commands. Security. Models. SecurityContacts. PSSecurityContact</span><span class="sxs-lookup"><span data-stu-id="e097e-134">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span></span>

## <span data-ttu-id="e097e-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="e097e-135">NOTES</span></span>

## <span data-ttu-id="e097e-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e097e-136">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityContact.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityContact.md
ms.openlocfilehash: 30586dcbbc08c31bf9b9fe65886fd2f487398618
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495658"
---
# <span data-ttu-id="34aab-101">Set-AzureRmSecurityContact</span><span class="sxs-lookup"><span data-stu-id="34aab-101">Set-AzureRmSecurityContact</span></span>

## <span data-ttu-id="34aab-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="34aab-102">SYNOPSIS</span></span>
<span data-ttu-id="34aab-103">Aktualisiert einen Sicherheitskontakt für ein Abonnement.</span><span class="sxs-lookup"><span data-stu-id="34aab-103">Updates a security contact for a subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="34aab-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="34aab-104">SYNTAX</span></span>

```
Set-AzureRmSecurityContact -Name <String> -Email <String> -Phone <String> [-AlertAdmin] [-NotifyOnAlert]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34aab-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="34aab-105">DESCRIPTION</span></span>
<span data-ttu-id="34aab-106">Aktualisiert einen Sicherheitskontakt für ein Abonnement.</span><span class="sxs-lookup"><span data-stu-id="34aab-106">Updates a security contact for a subscription.</span></span>

## <span data-ttu-id="34aab-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="34aab-107">EXAMPLES</span></span>

### <span data-ttu-id="34aab-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="34aab-108">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmSecurityContact -Name "default1" -Email "john@contoso.com" -Phone "214275-4038" -AlertAdmin -NotifyOnAlert

Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/securityContacts/
                     default1
Name               : default1
Email              : john@contoso.com
Phone              : 214275-4038
AlertNotifications : On
AlertsToAdmins     : On
```

<span data-ttu-id="34aab-109">Aktualisiert einen Sicherheitskontakt für ein Abonnement.</span><span class="sxs-lookup"><span data-stu-id="34aab-109">Updates a security contact for a subscription.</span></span>

## <span data-ttu-id="34aab-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="34aab-110">PARAMETERS</span></span>

### <span data-ttu-id="34aab-111">-AlertAdmin</span><span class="sxs-lookup"><span data-stu-id="34aab-111">-AlertAdmin</span></span>
<span data-ttu-id="34aab-112">Benachrichtigungen an Administratoren.</span><span class="sxs-lookup"><span data-stu-id="34aab-112">Alerts To Administrators.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34aab-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34aab-113">-DefaultProfile</span></span>
<span data-ttu-id="34aab-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="34aab-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34aab-115">– E-Mail</span><span class="sxs-lookup"><span data-stu-id="34aab-115">-Email</span></span>
<span data-ttu-id="34aab-116">E-Mail.</span><span class="sxs-lookup"><span data-stu-id="34aab-116">E-Mail.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34aab-117">-Name</span><span class="sxs-lookup"><span data-stu-id="34aab-117">-Name</span></span>
<span data-ttu-id="34aab-118">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="34aab-118">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34aab-119">-NotifyOnAlert</span><span class="sxs-lookup"><span data-stu-id="34aab-119">-NotifyOnAlert</span></span>
<span data-ttu-id="34aab-120">Benachrichtigungs Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="34aab-120">Alert Notifications.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34aab-121">-Telefon</span><span class="sxs-lookup"><span data-stu-id="34aab-121">-Phone</span></span>
<span data-ttu-id="34aab-122">Telefon.</span><span class="sxs-lookup"><span data-stu-id="34aab-122">Phone.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34aab-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="34aab-123">-Confirm</span></span>
<span data-ttu-id="34aab-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="34aab-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34aab-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34aab-125">-WhatIf</span></span>
<span data-ttu-id="34aab-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="34aab-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="34aab-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="34aab-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34aab-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34aab-128">CommonParameters</span></span>
<span data-ttu-id="34aab-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34aab-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34aab-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34aab-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34aab-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="34aab-131">INPUTS</span></span>

### <span data-ttu-id="34aab-132">System. String</span><span class="sxs-lookup"><span data-stu-id="34aab-132">System.String</span></span>

## <span data-ttu-id="34aab-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="34aab-133">OUTPUTS</span></span>

### <span data-ttu-id="34aab-134">Microsoft. Azure. Commands. Security. Models. SecurityContacts. PSSecurityContact</span><span class="sxs-lookup"><span data-stu-id="34aab-134">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span></span>

## <span data-ttu-id="34aab-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="34aab-135">NOTES</span></span>

## <span data-ttu-id="34aab-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="34aab-136">RELATED LINKS</span></span>

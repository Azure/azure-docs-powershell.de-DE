---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermadgroup
schema: 2.0.0
ms.openlocfilehash: fa9f708355e9c2fd4df530955db1d893e7591740
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849487"
---
# <span data-ttu-id="8be45-101">New-AzureRmADGroup</span><span class="sxs-lookup"><span data-stu-id="8be45-101">New-AzureRmADGroup</span></span>

## <span data-ttu-id="8be45-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8be45-102">SYNOPSIS</span></span>
<span data-ttu-id="8be45-103">Erstellt eine neue Active Directory-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="8be45-103">Creates a new active directory group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8be45-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8be45-104">SYNTAX</span></span>

```
New-AzureRmADGroup -DisplayName <String> -MailNickname <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8be45-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8be45-105">DESCRIPTION</span></span>
<span data-ttu-id="8be45-106">Erstellt eine neue Active Directory-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="8be45-106">Creates a new active directory group.</span></span>

## <span data-ttu-id="8be45-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8be45-107">EXAMPLES</span></span>

### <span data-ttu-id="8be45-108">Beispiel 1 – Erstellen einer neuen Anzeigengruppe</span><span class="sxs-lookup"><span data-stu-id="8be45-108">Example 1 - Create a new AD group</span></span>

```
PS C:\> New-AzureRmADGroup -DisplayName "MyGroupDisplayName" -MailNickname "myemail@domain.com"
```

<span data-ttu-id="8be45-109">Erstellt eine neue Anzeigengruppe mit dem Namen "MyGroupDisplayName" und dem e-Mail-Spitznamen " myemail@domain.com ".</span><span class="sxs-lookup"><span data-stu-id="8be45-109">Creates a new AD group with the name "MyGroupDisplayName" and the mail nickname "myemail@domain.com".</span></span>

## <span data-ttu-id="8be45-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="8be45-110">PARAMETERS</span></span>

### <span data-ttu-id="8be45-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8be45-111">-DefaultProfile</span></span>
<span data-ttu-id="8be45-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8be45-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8be45-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="8be45-113">-DisplayName</span></span>
<span data-ttu-id="8be45-114">Der Anzeigename für die Gruppe.</span><span class="sxs-lookup"><span data-stu-id="8be45-114">The display name for the group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8be45-115">-MailNickname</span><span class="sxs-lookup"><span data-stu-id="8be45-115">-MailNickname</span></span>
<span data-ttu-id="8be45-116">Der e-Mail-Spitznamen für die Gruppe.</span><span class="sxs-lookup"><span data-stu-id="8be45-116">The mail nickname for the group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8be45-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8be45-117">-Confirm</span></span>
<span data-ttu-id="8be45-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8be45-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8be45-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8be45-119">-WhatIf</span></span>
<span data-ttu-id="8be45-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8be45-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8be45-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8be45-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8be45-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8be45-122">CommonParameters</span></span>
<span data-ttu-id="8be45-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8be45-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8be45-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8be45-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8be45-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8be45-125">INPUTS</span></span>

### <span data-ttu-id="8be45-126">System. String</span><span class="sxs-lookup"><span data-stu-id="8be45-126">System.String</span></span>

## <span data-ttu-id="8be45-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8be45-127">OUTPUTS</span></span>

### <span data-ttu-id="8be45-128">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="8be45-128">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="8be45-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="8be45-129">NOTES</span></span>

## <span data-ttu-id="8be45-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8be45-130">RELATED LINKS</span></span>

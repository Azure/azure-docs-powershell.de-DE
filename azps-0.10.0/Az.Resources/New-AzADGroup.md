---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-Azadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzADGroup.md
ms.openlocfilehash: b5bc2f2eb99a8256dcaa6bc4f026d922f0f563ea
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843384"
---
# <span data-ttu-id="8a619-101">New-AzADGroup</span><span class="sxs-lookup"><span data-stu-id="8a619-101">New-AzADGroup</span></span>

## <span data-ttu-id="8a619-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8a619-102">SYNOPSIS</span></span>
<span data-ttu-id="8a619-103">Erstellt eine neue Active Directory-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="8a619-103">Creates a new active directory group.</span></span>

## <span data-ttu-id="8a619-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8a619-104">SYNTAX</span></span>

```
New-AzADGroup -DisplayName <String> -MailNickname <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a619-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8a619-105">DESCRIPTION</span></span>
<span data-ttu-id="8a619-106">Erstellt eine neue Active Directory-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="8a619-106">Creates a new active directory group.</span></span>

## <span data-ttu-id="8a619-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8a619-107">EXAMPLES</span></span>

### <span data-ttu-id="8a619-108">Beispiel 1 – Erstellen einer neuen Anzeigengruppe</span><span class="sxs-lookup"><span data-stu-id="8a619-108">Example 1 - Create a new AD group</span></span>

```
PS C:\> New-AzADGroup -DisplayName "MyGroupDisplayName" -MailNickname "myemail@domain.com"
```

<span data-ttu-id="8a619-109">Erstellt eine neue Anzeigengruppe mit dem Namen "MyGroupDisplayName" und dem e-Mail-Spitznamen " myemail@domain.com ".</span><span class="sxs-lookup"><span data-stu-id="8a619-109">Creates a new AD group with the name "MyGroupDisplayName" and the mail nickname "myemail@domain.com".</span></span>

## <span data-ttu-id="8a619-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="8a619-110">PARAMETERS</span></span>

### <span data-ttu-id="8a619-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a619-111">-DefaultProfile</span></span>
<span data-ttu-id="8a619-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8a619-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a619-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="8a619-113">-DisplayName</span></span>
<span data-ttu-id="8a619-114">Der Anzeigename für die Gruppe.</span><span class="sxs-lookup"><span data-stu-id="8a619-114">The display name for the group.</span></span>

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

### <span data-ttu-id="8a619-115">-MailNickname</span><span class="sxs-lookup"><span data-stu-id="8a619-115">-MailNickname</span></span>
<span data-ttu-id="8a619-116">Der e-Mail-Spitznamen für die Gruppe.</span><span class="sxs-lookup"><span data-stu-id="8a619-116">The mail nickname for the group.</span></span>

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

### <span data-ttu-id="8a619-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8a619-117">-Confirm</span></span>
<span data-ttu-id="8a619-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8a619-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a619-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a619-119">-WhatIf</span></span>
<span data-ttu-id="8a619-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8a619-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a619-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8a619-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a619-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a619-122">CommonParameters</span></span>
<span data-ttu-id="8a619-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a619-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a619-124">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a619-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a619-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8a619-125">INPUTS</span></span>

### <span data-ttu-id="8a619-126">System. String</span><span class="sxs-lookup"><span data-stu-id="8a619-126">System.String</span></span>

## <span data-ttu-id="8a619-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8a619-127">OUTPUTS</span></span>

### <span data-ttu-id="8a619-128">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="8a619-128">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="8a619-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="8a619-129">NOTES</span></span>

## <span data-ttu-id="8a619-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8a619-130">RELATED LINKS</span></span>

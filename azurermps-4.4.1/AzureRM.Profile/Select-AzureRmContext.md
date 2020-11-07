---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Select-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Select-AzureRmContext.md
ms.openlocfilehash: 5450939ba5d0dc2fb1ae6c475d51b6fc9187082c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663550"
---
# <span data-ttu-id="d460e-101">Select-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="d460e-101">Select-AzureRmContext</span></span>

## <span data-ttu-id="d460e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d460e-102">SYNOPSIS</span></span>
<span data-ttu-id="d460e-103">Wählen Sie ein Abonnement und ein Konto für das Ziel in Azure PowerShell-Cmdlets aus.</span><span class="sxs-lookup"><span data-stu-id="d460e-103">Select a subscription and account to target in Azure PowerShell cmdlets</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d460e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d460e-104">SYNTAX</span></span>

### <span data-ttu-id="d460e-105">Eingabeobjekt (Standard)</span><span class="sxs-lookup"><span data-stu-id="d460e-105">Input Object (Default)</span></span>
```
Select-AzureRmContext -InputObject <PSAzureContext> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d460e-106">Kontext Name</span><span class="sxs-lookup"><span data-stu-id="d460e-106">Context Name</span></span>
```
Select-AzureRmContext [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="d460e-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d460e-107">DESCRIPTION</span></span>
<span data-ttu-id="d460e-108">Wählen Sie in Azure PowerShell-Cmdlets ein Abonnement für Target (oder Konto oder Mandant) aus.</span><span class="sxs-lookup"><span data-stu-id="d460e-108">Select a  subscription to target (or account or tenant) in Azure PowerShell cmdlets.</span></span>  <span data-ttu-id="d460e-109">Nach diesem Cmdlet werden zukünftige Cmdlets auf den ausgewählten Kontext ausgerichtet.</span><span class="sxs-lookup"><span data-stu-id="d460e-109">After this cmdlet, future cmdlets will target the selected context.</span></span>

## <span data-ttu-id="d460e-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d460e-110">EXAMPLES</span></span>

### <span data-ttu-id="d460e-111">Beispiel 1: Ziel eines benannten Kontexts</span><span class="sxs-lookup"><span data-stu-id="d460e-111">Example 1 : Target a named context</span></span>
```
PS C:\> Select-AzureRmContext "Work"
```

<span data-ttu-id="d460e-112">Ziel der zukünftigen Azure PowerShell-Cmdlets für das Konto, den Mandanten und das Abonnement im Kontext "Arbeit".</span><span class="sxs-lookup"><span data-stu-id="d460e-112">Target future Azure PowerShell cmdlets at the account, tenant, and subscription in the 'Work' context.</span></span>

## <span data-ttu-id="d460e-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="d460e-113">PARAMETERS</span></span>

### <span data-ttu-id="d460e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d460e-114">-DefaultProfile</span></span>
<span data-ttu-id="d460e-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, Mandanten und Abonnements</span><span class="sxs-lookup"><span data-stu-id="d460e-115">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d460e-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d460e-116">-InputObject</span></span>
<span data-ttu-id="d460e-117">Ein Kontextobjekt, das normalerweise durch die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="d460e-117">A context object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.PSAzureContext
Parameter Sets: Input Object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d460e-118">-Name</span><span class="sxs-lookup"><span data-stu-id="d460e-118">-Name</span></span>
<span data-ttu-id="d460e-119">Der Name des Kontexts</span><span class="sxs-lookup"><span data-stu-id="d460e-119">The name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: Context Name
Aliases: 
Accepted values: [contrib@AzureSDKTeam.onmicrosoft.com, 0b1f6471-1bf0-4dda-aec3-cb9272f09590], [markcowl@microsoft.com, 00977cdb-163f-435f-9c32-39ec8ae61f4d]

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d460e-120">-Scope</span><span class="sxs-lookup"><span data-stu-id="d460e-120">-Scope</span></span>
<span data-ttu-id="d460e-121">Bestimmt den Bereich von Kontextänderungen, beispielsweise wheher Änderungen gelten nur für den cusrrent-Prozess oder für alle von diesem Benutzer gestarteten Sitzungen.</span><span class="sxs-lookup"><span data-stu-id="d460e-121">Determines the scope of context changes, for example, wheher changes apply only to the cusrrent process, or to all sessions started by this user</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases: 
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d460e-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d460e-122">-Confirm</span></span>
<span data-ttu-id="d460e-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d460e-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d460e-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d460e-124">-WhatIf</span></span>
<span data-ttu-id="d460e-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d460e-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d460e-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d460e-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d460e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d460e-127">CommonParameters</span></span>
<span data-ttu-id="d460e-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d460e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d460e-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d460e-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d460e-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d460e-130">INPUTS</span></span>

### <span data-ttu-id="d460e-131">Keine</span><span class="sxs-lookup"><span data-stu-id="d460e-131">None</span></span>

## <span data-ttu-id="d460e-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d460e-132">OUTPUTS</span></span>

### <span data-ttu-id="d460e-133">Microsoft. Azure. Commands. profile. Models. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="d460e-133">Microsoft.Azure.Commands.Profile.Models.PSAzureContext</span></span>

## <span data-ttu-id="d460e-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="d460e-134">NOTES</span></span>

## <span data-ttu-id="d460e-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d460e-135">RELATED LINKS</span></span>


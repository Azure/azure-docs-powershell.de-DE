---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSqlInformationProtectionPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSqlInformationProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSqlInformationProtectionPolicy.md
ms.openlocfilehash: 3b433860cda56f827bb58bc135240da41b89ef93
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471991"
---
# <span data-ttu-id="b0ed8-101">Set-AzSqlInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="b0ed8-101">Set-AzSqlInformationProtectionPolicy</span></span>

## <span data-ttu-id="b0ed8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0ed8-102">SYNOPSIS</span></span>
<span data-ttu-id="b0ed8-103">Legt den effektiven Mandanten SQL Informationsschutzrichtlinie fest.</span><span class="sxs-lookup"><span data-stu-id="b0ed8-103">Sets the effective tenant SQL information protection policy.</span></span>

## <span data-ttu-id="b0ed8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b0ed8-104">SYNTAX</span></span>

### <span data-ttu-id="b0ed8-105">SQL Informationsschutzrichtlinie (Standard)</span><span class="sxs-lookup"><span data-stu-id="b0ed8-105">SQL Information Protection Policy (Default)</span></span>
```
Set-AzSqlInformationProtectionPolicy -Policy <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0ed8-106">SQL des Dateipfads der Informationsschutzrichtlinie</span><span class="sxs-lookup"><span data-stu-id="b0ed8-106">SQL Information Protection Policy File Path</span></span>
```
Set-AzSqlInformationProtectionPolicy -FilePath <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0ed8-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b0ed8-107">DESCRIPTION</span></span>
<span data-ttu-id="b0ed8-108">Legt den effektiven Mandanten SQL Informationsschutzrichtlinie fest.</span><span class="sxs-lookup"><span data-stu-id="b0ed8-108">Sets the effective tenant SQL information protection policy.</span></span>

## <span data-ttu-id="b0ed8-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b0ed8-109">EXAMPLES</span></span>

### <span data-ttu-id="b0ed8-110">Beispiel</span><span class="sxs-lookup"><span data-stu-id="b0ed8-110">Example</span></span>
```powershell
PS C:\> Set-AzSqlInformationProtectionPolicy -FilePath "C:\Users\myUser\Desktop\policy.json"
```

## <span data-ttu-id="b0ed8-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b0ed8-111">PARAMETERS</span></span>

### <span data-ttu-id="b0ed8-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b0ed8-112">-AsJob</span></span>
<span data-ttu-id="b0ed8-113">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="b0ed8-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b0ed8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0ed8-114">-DefaultProfile</span></span>
<span data-ttu-id="b0ed8-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b0ed8-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0ed8-116">-FilePath</span><span class="sxs-lookup"><span data-stu-id="b0ed8-116">-FilePath</span></span>
<span data-ttu-id="b0ed8-117">Gibt einen Pfad einer JSON-Datei an, die SQL Information Protection Policy Definition enthält.</span><span class="sxs-lookup"><span data-stu-id="b0ed8-117">Specifies a path of a .json file containing SQL Information Protection Policy definition.</span></span>

```yaml
Type: System.String
Parameter Sets: SQL Information Protection Policy File Path
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0ed8-118">-Policy</span><span class="sxs-lookup"><span data-stu-id="b0ed8-118">-Policy</span></span>
<span data-ttu-id="b0ed8-119">Gibt eine SQL informationsschutzrichtliniendefinition an.</span><span class="sxs-lookup"><span data-stu-id="b0ed8-119">Specifies a SQL information protection policy definition.</span></span> <span data-ttu-id="b0ed8-120">Sie können einen Pfad einer JSON-Datei oder eine JSON-Formatzeichenfolge angeben, die die Richtlinie definiert.</span><span class="sxs-lookup"><span data-stu-id="b0ed8-120">You can specify a path of a .json file or a JSON format string that defines the policy.</span></span>

```yaml
Type: System.String
Parameter Sets: SQL Information Protection Policy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0ed8-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b0ed8-121">-Confirm</span></span>
<span data-ttu-id="b0ed8-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b0ed8-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0ed8-123">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="b0ed8-123">-WhatIf</span></span>
<span data-ttu-id="b0ed8-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b0ed8-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b0ed8-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b0ed8-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0ed8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0ed8-126">CommonParameters</span></span>
<span data-ttu-id="b0ed8-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0ed8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0ed8-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b0ed8-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0ed8-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b0ed8-129">INPUTS</span></span>

### <span data-ttu-id="b0ed8-130">System.String</span><span class="sxs-lookup"><span data-stu-id="b0ed8-130">System.String</span></span>

## <span data-ttu-id="b0ed8-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b0ed8-131">OUTPUTS</span></span>

### <span data-ttu-id="b0ed8-132">Microsoft.Azure.Commands.SecurityCenter.Models.SqlInformationProtectionPolicy.PSSqlInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="b0ed8-132">Microsoft.Azure.Commands.SecurityCenter.Models.SqlInformationProtectionPolicy.PSSqlInformationProtectionPolicy</span></span>

## <span data-ttu-id="b0ed8-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b0ed8-133">NOTES</span></span>

## <span data-ttu-id="b0ed8-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b0ed8-134">RELATED LINKS</span></span>

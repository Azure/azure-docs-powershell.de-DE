---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSqlInformationProtectionPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSqlInformationProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSqlInformationProtectionPolicy.md
ms.openlocfilehash: 3b433860cda56f827bb58bc135240da41b89ef93
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165572"
---
# <span data-ttu-id="1905c-101">Set-AzSqlInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="1905c-101">Set-AzSqlInformationProtectionPolicy</span></span>

## <span data-ttu-id="1905c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1905c-102">SYNOPSIS</span></span>
<span data-ttu-id="1905c-103">Legt die effektive Mandanten-SQL-Informationsschutz Richtlinie fest.</span><span class="sxs-lookup"><span data-stu-id="1905c-103">Sets the effective tenant SQL information protection policy.</span></span>

## <span data-ttu-id="1905c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1905c-104">SYNTAX</span></span>

### <span data-ttu-id="1905c-105">SQL-Informationsschutz Richtlinie (Standard)</span><span class="sxs-lookup"><span data-stu-id="1905c-105">SQL Information Protection Policy (Default)</span></span>
```
Set-AzSqlInformationProtectionPolicy -Policy <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1905c-106">SQL-Informationsschutz Richtlinien-Dateipfad</span><span class="sxs-lookup"><span data-stu-id="1905c-106">SQL Information Protection Policy File Path</span></span>
```
Set-AzSqlInformationProtectionPolicy -FilePath <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1905c-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1905c-107">DESCRIPTION</span></span>
<span data-ttu-id="1905c-108">Legt die effektive Mandanten-SQL-Informationsschutz Richtlinie fest.</span><span class="sxs-lookup"><span data-stu-id="1905c-108">Sets the effective tenant SQL information protection policy.</span></span>

## <span data-ttu-id="1905c-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1905c-109">EXAMPLES</span></span>

### <span data-ttu-id="1905c-110">Beispiel</span><span class="sxs-lookup"><span data-stu-id="1905c-110">Example</span></span>
```powershell
PS C:\> Set-AzSqlInformationProtectionPolicy -FilePath "C:\Users\myUser\Desktop\policy.json"
```

## <span data-ttu-id="1905c-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="1905c-111">PARAMETERS</span></span>

### <span data-ttu-id="1905c-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1905c-112">-AsJob</span></span>
<span data-ttu-id="1905c-113">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="1905c-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1905c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1905c-114">-DefaultProfile</span></span>
<span data-ttu-id="1905c-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1905c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1905c-116">-FilePath</span><span class="sxs-lookup"><span data-stu-id="1905c-116">-FilePath</span></span>
<span data-ttu-id="1905c-117">Gibt den Pfad einer JSON-Datei an, die die Definition der SQL-Informationsschutz Richtlinie enthält.</span><span class="sxs-lookup"><span data-stu-id="1905c-117">Specifies a path of a .json file containing SQL Information Protection Policy definition.</span></span>

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

### <span data-ttu-id="1905c-118">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="1905c-118">-Policy</span></span>
<span data-ttu-id="1905c-119">Gibt eine SQL-Informationsschutz-Richtliniendefinition an.</span><span class="sxs-lookup"><span data-stu-id="1905c-119">Specifies a SQL information protection policy definition.</span></span> <span data-ttu-id="1905c-120">Sie können einen Pfad einer JSON-Datei oder eine JSON-Formatzeichenfolge angeben, die die Richtlinie definiert.</span><span class="sxs-lookup"><span data-stu-id="1905c-120">You can specify a path of a .json file or a JSON format string that defines the policy.</span></span>

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

### <span data-ttu-id="1905c-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1905c-121">-Confirm</span></span>
<span data-ttu-id="1905c-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1905c-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1905c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1905c-123">-WhatIf</span></span>
<span data-ttu-id="1905c-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1905c-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1905c-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1905c-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1905c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1905c-126">CommonParameters</span></span>
<span data-ttu-id="1905c-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1905c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1905c-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1905c-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1905c-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1905c-129">INPUTS</span></span>

### <span data-ttu-id="1905c-130">System. String</span><span class="sxs-lookup"><span data-stu-id="1905c-130">System.String</span></span>

## <span data-ttu-id="1905c-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1905c-131">OUTPUTS</span></span>

### <span data-ttu-id="1905c-132">Microsoft. Azure. Commands. SecurityCenter. Models. SqlInformationProtectionPolicy. PSSqlInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="1905c-132">Microsoft.Azure.Commands.SecurityCenter.Models.SqlInformationProtectionPolicy.PSSqlInformationProtectionPolicy</span></span>

## <span data-ttu-id="1905c-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="1905c-133">NOTES</span></span>

## <span data-ttu-id="1905c-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1905c-134">RELATED LINKS</span></span>

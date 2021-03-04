---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/set-azdataboxedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeUser.md
ms.openlocfilehash: a2de03f28935fb8002966e0e9251218809ddec5b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928251"
---
# <span data-ttu-id="7617b-101">Set-AzDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="7617b-101">Set-AzDataBoxEdgeUser</span></span>

## <span data-ttu-id="7617b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7617b-102">SYNOPSIS</span></span>
<span data-ttu-id="7617b-103">Legt ein neues Kennwort für einen Benutzer auf dem Gerät fest.</span><span class="sxs-lookup"><span data-stu-id="7617b-103">Sets a new password for a user on the device.</span></span>

## <span data-ttu-id="7617b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7617b-104">SYNTAX</span></span>

### <span data-ttu-id="7617b-105">SetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="7617b-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -Password <SecureString> -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7617b-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7617b-106">SetByResourceIdParameterSet</span></span>
```
Set-AzDataBoxEdgeUser -ResourceId <String> -Password <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7617b-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7617b-107">SetByInputObjectParameterSet</span></span>
```
Set-AzDataBoxEdgeUser -InputObject <PSDataBoxEdgeUser> -Password <SecureString> -EncryptionKey <SecureString>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7617b-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7617b-108">DESCRIPTION</span></span>
<span data-ttu-id="7617b-109">Das **Cmdlet Set-AzDataBoxEdgeUser** legt ein neues Kennwort für einen Benutzer auf dem Data Box Edge-Gerät fest.</span><span class="sxs-lookup"><span data-stu-id="7617b-109">The **Set-AzDataBoxEdgeUser** cmdlet sets a new password for a user on the Data Box Edge device.</span></span>

## <span data-ttu-id="7617b-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7617b-110">EXAMPLES</span></span>

### <span data-ttu-id="7617b-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7617b-111">Example 1</span></span>
```powershell
PS C:\> Set-AzDataBoxEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
 -Password @SecureString -EncryptionKey @SecureString
```

## <span data-ttu-id="7617b-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="7617b-112">PARAMETERS</span></span>

### <span data-ttu-id="7617b-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7617b-113">-AsJob</span></span>
<span data-ttu-id="7617b-114">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="7617b-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7617b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7617b-115">-DefaultProfile</span></span>
<span data-ttu-id="7617b-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7617b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7617b-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="7617b-117">-DeviceName</span></span>
<span data-ttu-id="7617b-118">Gerätename</span><span class="sxs-lookup"><span data-stu-id="7617b-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7617b-119">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="7617b-119">-EncryptionKey</span></span>
<span data-ttu-id="7617b-120">Verschlüsselungsschlüssel des Edgegeräts</span><span class="sxs-lookup"><span data-stu-id="7617b-120">Encryption key of the Edge device</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7617b-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7617b-121">-InputObject</span></span>
<span data-ttu-id="7617b-122">Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="7617b-122">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7617b-123">-Name</span><span class="sxs-lookup"><span data-stu-id="7617b-123">-Name</span></span>
<span data-ttu-id="7617b-124">Benutzername</span><span class="sxs-lookup"><span data-stu-id="7617b-124">Username</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7617b-125">-Password</span><span class="sxs-lookup"><span data-stu-id="7617b-125">-Password</span></span>
<span data-ttu-id="7617b-126">Kennwort als sichere Zeichenfolge angeben</span><span class="sxs-lookup"><span data-stu-id="7617b-126">Password, provide as a secure string</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7617b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7617b-127">-ResourceGroupName</span></span>
<span data-ttu-id="7617b-128">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="7617b-128">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7617b-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7617b-129">-ResourceId</span></span>
<span data-ttu-id="7617b-130">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="7617b-130">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7617b-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7617b-131">-Confirm</span></span>
<span data-ttu-id="7617b-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7617b-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7617b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7617b-133">-WhatIf</span></span>
<span data-ttu-id="7617b-134">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7617b-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7617b-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7617b-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7617b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7617b-136">CommonParameters</span></span>
<span data-ttu-id="7617b-137">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7617b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7617b-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7617b-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7617b-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7617b-139">INPUTS</span></span>

### <span data-ttu-id="7617b-140">Keine</span><span class="sxs-lookup"><span data-stu-id="7617b-140">None</span></span>

## <span data-ttu-id="7617b-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7617b-141">OUTPUTS</span></span>

### <span data-ttu-id="7617b-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="7617b-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span></span>

## <span data-ttu-id="7617b-143">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="7617b-143">NOTES</span></span>

## <span data-ttu-id="7617b-144">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="7617b-144">RELATED LINKS</span></span>

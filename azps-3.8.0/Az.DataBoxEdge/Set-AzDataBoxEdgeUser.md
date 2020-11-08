---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/set-azdataboxedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeUser.md
ms.openlocfilehash: 9074de6f4e6ee02a1476c1112d870b45d5bf6ccf
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996774"
---
# <span data-ttu-id="b0c1e-101">Set-AzDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="b0c1e-101">Set-AzDataBoxEdgeUser</span></span>

## <span data-ttu-id="b0c1e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b0c1e-102">SYNOPSIS</span></span>
<span data-ttu-id="b0c1e-103">Legt ein neues Kennwort für einen Benutzer auf dem Gerät fest.</span><span class="sxs-lookup"><span data-stu-id="b0c1e-103">Sets a new password for a user on the device.</span></span>

## <span data-ttu-id="b0c1e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b0c1e-104">SYNTAX</span></span>

### <span data-ttu-id="b0c1e-105">SetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="b0c1e-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -Password <SecureString> -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0c1e-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b0c1e-106">SetByResourceIdParameterSet</span></span>
```
Set-AzDataBoxEdgeUser -ResourceId <String> -Password <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0c1e-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b0c1e-107">SetByInputObjectParameterSet</span></span>
```
Set-AzDataBoxEdgeUser -InputObject <PSDataBoxEdgeUser> -Password <SecureString> -EncryptionKey <SecureString>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0c1e-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b0c1e-108">DESCRIPTION</span></span>
<span data-ttu-id="b0c1e-109">Das Cmdlet " **Set-AzDataBoxEdgeUser** " legt ein neues Kennwort für einen Benutzer auf dem Daten Feld-Edge-Gerät fest.</span><span class="sxs-lookup"><span data-stu-id="b0c1e-109">The **Set-AzDataBoxEdgeUser** cmdlet sets a new password for a user on the Data Box Edge device.</span></span>

## <span data-ttu-id="b0c1e-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b0c1e-110">EXAMPLES</span></span>

### <span data-ttu-id="b0c1e-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b0c1e-111">Example 1</span></span>
```powershell
PS C:\> Set-AzDataBoxEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
 -Password @SecureString -EncryptionKey @SecureString
```

## <span data-ttu-id="b0c1e-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="b0c1e-112">PARAMETERS</span></span>

### <span data-ttu-id="b0c1e-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b0c1e-113">-AsJob</span></span>
<span data-ttu-id="b0c1e-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="b0c1e-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b0c1e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0c1e-115">-DefaultProfile</span></span>
<span data-ttu-id="b0c1e-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b0c1e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0c1e-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="b0c1e-117">-DeviceName</span></span>
<span data-ttu-id="b0c1e-118">Geräte Name</span><span class="sxs-lookup"><span data-stu-id="b0c1e-118">Device Name</span></span>

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

### <span data-ttu-id="b0c1e-119">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="b0c1e-119">-EncryptionKey</span></span>
<span data-ttu-id="b0c1e-120">Verschlüsselungsschlüssel des Edge-Geräts</span><span class="sxs-lookup"><span data-stu-id="b0c1e-120">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="b0c1e-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b0c1e-121">-InputObject</span></span>
<span data-ttu-id="b0c1e-122">Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="b0c1e-122">Input Object</span></span>

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

### <span data-ttu-id="b0c1e-123">-Name</span><span class="sxs-lookup"><span data-stu-id="b0c1e-123">-Name</span></span>
<span data-ttu-id="b0c1e-124">Username</span><span class="sxs-lookup"><span data-stu-id="b0c1e-124">Username</span></span>

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

### <span data-ttu-id="b0c1e-125">-Kennwort</span><span class="sxs-lookup"><span data-stu-id="b0c1e-125">-Password</span></span>
<span data-ttu-id="b0c1e-126">Kennwort, als sichere Zeichenfolge bereitstellen</span><span class="sxs-lookup"><span data-stu-id="b0c1e-126">Password, provide as a secure string</span></span>

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

### <span data-ttu-id="b0c1e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0c1e-127">-ResourceGroupName</span></span>
<span data-ttu-id="b0c1e-128">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="b0c1e-128">Resource Group Name</span></span>

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

### <span data-ttu-id="b0c1e-129">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="b0c1e-129">-ResourceId</span></span>
<span data-ttu-id="b0c1e-130">Azure-Hilfsquelle</span><span class="sxs-lookup"><span data-stu-id="b0c1e-130">Azure ResourceId</span></span>

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

### <span data-ttu-id="b0c1e-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b0c1e-131">-Confirm</span></span>
<span data-ttu-id="b0c1e-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b0c1e-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0c1e-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0c1e-133">-WhatIf</span></span>
<span data-ttu-id="b0c1e-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b0c1e-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b0c1e-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b0c1e-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0c1e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0c1e-136">CommonParameters</span></span>
<span data-ttu-id="b0c1e-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0c1e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0c1e-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b0c1e-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0c1e-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b0c1e-139">INPUTS</span></span>

### <span data-ttu-id="b0c1e-140">Keine</span><span class="sxs-lookup"><span data-stu-id="b0c1e-140">None</span></span>

## <span data-ttu-id="b0c1e-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b0c1e-141">OUTPUTS</span></span>

### <span data-ttu-id="b0c1e-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="b0c1e-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span></span>

## <span data-ttu-id="b0c1e-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="b0c1e-143">NOTES</span></span>

## <span data-ttu-id="b0c1e-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b0c1e-144">RELATED LINKS</span></span>

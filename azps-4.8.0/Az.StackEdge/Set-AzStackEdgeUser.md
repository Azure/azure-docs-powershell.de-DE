---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/set-azstackedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeUser.md
ms.openlocfilehash: 707889590efeb17ee676fe3d8b37325bc48fdc81
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173402"
---
# <span data-ttu-id="a1213-101">Set-AzStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="a1213-101">Set-AzStackEdgeUser</span></span>

## <span data-ttu-id="a1213-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a1213-102">SYNOPSIS</span></span>
<span data-ttu-id="a1213-103">Legt ein neues Kennwort für einen Benutzer auf dem Gerät fest.</span><span class="sxs-lookup"><span data-stu-id="a1213-103">Sets a new password for a user on the device.</span></span>

## <span data-ttu-id="a1213-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a1213-104">SYNTAX</span></span>

### <span data-ttu-id="a1213-105">SetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="a1213-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzStackEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -Password <SecureString> -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1213-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a1213-106">SetByResourceIdParameterSet</span></span>
```
Set-AzStackEdgeUser -ResourceId <String> -Password <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1213-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a1213-107">SetByInputObjectParameterSet</span></span>
```
Set-AzStackEdgeUser -InputObject <PSStackEdgeUser> -Password <SecureString> -EncryptionKey <SecureString>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1213-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a1213-108">DESCRIPTION</span></span>
<span data-ttu-id="a1213-109">Das Cmdlet " **Set-AzStackEdgeUser** " legt ein neues Kennwort für einen Benutzer auf dem Stack-Edge-Gerät fest.</span><span class="sxs-lookup"><span data-stu-id="a1213-109">The **Set-AzStackEdgeUser** cmdlet sets a new password for a user on the Stack Edge device.</span></span>

## <span data-ttu-id="a1213-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a1213-110">EXAMPLES</span></span>

### <span data-ttu-id="a1213-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a1213-111">Example 1</span></span>
```powershell
PS C:\> Set-AzStackEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
 -Password @SecureString -EncryptionKey @SecureString
```

## <span data-ttu-id="a1213-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="a1213-112">PARAMETERS</span></span>

### <span data-ttu-id="a1213-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a1213-113">-AsJob</span></span>
<span data-ttu-id="a1213-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="a1213-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a1213-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1213-115">-DefaultProfile</span></span>
<span data-ttu-id="a1213-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a1213-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1213-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="a1213-117">-DeviceName</span></span>
<span data-ttu-id="a1213-118">Geräte Name</span><span class="sxs-lookup"><span data-stu-id="a1213-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1213-119">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="a1213-119">-EncryptionKey</span></span>
<span data-ttu-id="a1213-120">Verschlüsselungsschlüssel des Edge-Geräts</span><span class="sxs-lookup"><span data-stu-id="a1213-120">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="a1213-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a1213-121">-InputObject</span></span>
<span data-ttu-id="a1213-122">Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="a1213-122">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser
Parameter Sets: SetByInputObjectParameterSet
Aliases: User

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1213-123">-Name</span><span class="sxs-lookup"><span data-stu-id="a1213-123">-Name</span></span>
<span data-ttu-id="a1213-124">Username</span><span class="sxs-lookup"><span data-stu-id="a1213-124">Username</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: Username

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1213-125">-Kennwort</span><span class="sxs-lookup"><span data-stu-id="a1213-125">-Password</span></span>
<span data-ttu-id="a1213-126">Kennwort, als sichere Zeichenfolge bereitstellen</span><span class="sxs-lookup"><span data-stu-id="a1213-126">Password, provide as a secure string</span></span>

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

### <span data-ttu-id="a1213-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1213-127">-ResourceGroupName</span></span>
<span data-ttu-id="a1213-128">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="a1213-128">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1213-129">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="a1213-129">-ResourceId</span></span>
<span data-ttu-id="a1213-130">Azure-Hilfsquelle</span><span class="sxs-lookup"><span data-stu-id="a1213-130">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1213-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a1213-131">-Confirm</span></span>
<span data-ttu-id="a1213-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a1213-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1213-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1213-133">-WhatIf</span></span>
<span data-ttu-id="a1213-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a1213-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a1213-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a1213-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1213-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1213-136">CommonParameters</span></span>
<span data-ttu-id="a1213-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1213-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1213-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a1213-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1213-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a1213-139">INPUTS</span></span>

### <span data-ttu-id="a1213-140">Keine</span><span class="sxs-lookup"><span data-stu-id="a1213-140">None</span></span>

## <span data-ttu-id="a1213-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a1213-141">OUTPUTS</span></span>

### <span data-ttu-id="a1213-142">Microsoft. Azure. PowerShell. Cmdlets. StackEdge. Models. PSStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="a1213-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser</span></span>

## <span data-ttu-id="a1213-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="a1213-143">NOTES</span></span>

## <span data-ttu-id="a1213-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a1213-144">RELATED LINKS</span></span>

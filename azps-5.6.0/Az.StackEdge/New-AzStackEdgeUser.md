---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/new-azstackedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeUser.md
ms.openlocfilehash: cd904a913ce9ea0cdcc2d347463fa21ac7e13943
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101945539"
---
# <span data-ttu-id="90d62-101">New-AzStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="90d62-101">New-AzStackEdgeUser</span></span>

## <span data-ttu-id="90d62-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90d62-102">SYNOPSIS</span></span>
<span data-ttu-id="90d62-103">Erstellt einen neuen Benutzer für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="90d62-103">Creates a new user for the device.</span></span>

## <span data-ttu-id="90d62-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="90d62-104">SYNTAX</span></span>

```
New-AzStackEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -Password <SecureString> -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [[-Type] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90d62-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="90d62-105">DESCRIPTION</span></span>
<span data-ttu-id="90d62-106">Das **Cmdlet New-AzStackEdgeUser** erstellt einen neuen Benutzer für das Stack Edge-Gerät.</span><span class="sxs-lookup"><span data-stu-id="90d62-106">The **New-AzStackEdgeUser** cmdlet creates a new user for the Stack Edge device.</span></span> <span data-ttu-id="90d62-107">Die Erstellung von nur Benutzern vom Typ `Share` wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="90d62-107">Creation of only users of type `Share` is supported.</span></span>

## <span data-ttu-id="90d62-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="90d62-108">EXAMPLES</span></span>

### <span data-ttu-id="90d62-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="90d62-109">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
 -Password password-secured-string -EncryptionKey encryption-key
User name   Type  ResourceGroupName DeviceName
---------   ----  ----------------- ----------
username    Share resourceGroupName deviceName
```

```powershell
PS C:\> New-AzStackEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
 -Password password-secured-string -EncryptionKey encryption-key -Type Share
User name   Type  ResourceGroupName DeviceName
---------   ----  ----------------- ----------
username    Share resourceGroupName deviceName
```

## <span data-ttu-id="90d62-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="90d62-110">PARAMETERS</span></span>

### <span data-ttu-id="90d62-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="90d62-111">-AsJob</span></span>
<span data-ttu-id="90d62-112">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="90d62-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="90d62-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90d62-113">-DefaultProfile</span></span>
<span data-ttu-id="90d62-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="90d62-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90d62-115">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="90d62-115">-DeviceName</span></span>
<span data-ttu-id="90d62-116">Gerätename</span><span class="sxs-lookup"><span data-stu-id="90d62-116">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90d62-117">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="90d62-117">-EncryptionKey</span></span>
<span data-ttu-id="90d62-118">Verschlüsselungsschlüssel des Edgegeräts</span><span class="sxs-lookup"><span data-stu-id="90d62-118">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="90d62-119">-Name</span><span class="sxs-lookup"><span data-stu-id="90d62-119">-Name</span></span>
<span data-ttu-id="90d62-120">Benutzername</span><span class="sxs-lookup"><span data-stu-id="90d62-120">Username</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Username

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90d62-121">-Password</span><span class="sxs-lookup"><span data-stu-id="90d62-121">-Password</span></span>
<span data-ttu-id="90d62-122">Kennwort als sichere Zeichenfolge angeben</span><span class="sxs-lookup"><span data-stu-id="90d62-122">Password, provide as a secure string</span></span>

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

### <span data-ttu-id="90d62-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90d62-123">-ResourceGroupName</span></span>
<span data-ttu-id="90d62-124">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="90d62-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90d62-125">-Type</span><span class="sxs-lookup"><span data-stu-id="90d62-125">-Type</span></span>
<span data-ttu-id="90d62-126">Auswählen von UserType</span><span class="sxs-lookup"><span data-stu-id="90d62-126">Select UserType</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90d62-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="90d62-127">-Confirm</span></span>
<span data-ttu-id="90d62-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="90d62-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90d62-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90d62-129">-WhatIf</span></span>
<span data-ttu-id="90d62-130">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="90d62-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="90d62-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="90d62-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90d62-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90d62-132">CommonParameters</span></span>
<span data-ttu-id="90d62-133">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90d62-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90d62-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="90d62-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90d62-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="90d62-135">INPUTS</span></span>

### <span data-ttu-id="90d62-136">Keine</span><span class="sxs-lookup"><span data-stu-id="90d62-136">None</span></span>

## <span data-ttu-id="90d62-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="90d62-137">OUTPUTS</span></span>

### <span data-ttu-id="90d62-138">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="90d62-138">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="90d62-139">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="90d62-139">NOTES</span></span>

## <span data-ttu-id="90d62-140">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="90d62-140">RELATED LINKS</span></span>

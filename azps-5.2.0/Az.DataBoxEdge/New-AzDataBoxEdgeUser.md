---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeUser.md
ms.openlocfilehash: a53f67c12a5c8d125319fc19f69db3ea9a57c5e1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98307832"
---
# <span data-ttu-id="f2d6f-101">New-AzDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="f2d6f-101">New-AzDataBoxEdgeUser</span></span>

## <span data-ttu-id="f2d6f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2d6f-102">SYNOPSIS</span></span>
<span data-ttu-id="f2d6f-103">Erstellt einen neuen Benutzer für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="f2d6f-103">Creates a new user for the device.</span></span>

## <span data-ttu-id="f2d6f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f2d6f-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -Password <SecureString> -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [[-Type] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2d6f-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f2d6f-105">DESCRIPTION</span></span>
<span data-ttu-id="f2d6f-106">Das **Cmdlet "New-AzDataBoxEdgeUser"** erstellt einen neuen Benutzer für das Edgegerät "Data Box".</span><span class="sxs-lookup"><span data-stu-id="f2d6f-106">The **New-AzDataBoxEdgeUser** cmdlet creates a new user for the Data Box Edge device.</span></span> <span data-ttu-id="f2d6f-107">Die Erstellung nur von Typbenutzern `Share` wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f2d6f-107">Creation of only users of type `Share` is supported.</span></span>

## <span data-ttu-id="f2d6f-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f2d6f-108">EXAMPLES</span></span>

### <span data-ttu-id="f2d6f-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f2d6f-109">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
 -Password password-secured-string -EncryptionKey encryption-key
User name   Type  ResourceGroupName DeviceName
---------   ----  ----------------- ----------
username    Share resourceGroupName deviceName
```

```powershell
PS C:\> New-AzDataBoxEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
 -Password password-secured-string -EncryptionKey encryption-key -Type Share
User name   Type  ResourceGroupName DeviceName
---------   ----  ----------------- ----------
username    Share resourceGroupName deviceName
```

## <span data-ttu-id="f2d6f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f2d6f-110">PARAMETERS</span></span>

### <span data-ttu-id="f2d6f-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f2d6f-111">-AsJob</span></span>
<span data-ttu-id="f2d6f-112">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="f2d6f-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f2d6f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2d6f-113">-DefaultProfile</span></span>
<span data-ttu-id="f2d6f-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f2d6f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2d6f-115">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="f2d6f-115">-DeviceName</span></span>
<span data-ttu-id="f2d6f-116">Gerätename</span><span class="sxs-lookup"><span data-stu-id="f2d6f-116">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2d6f-117">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="f2d6f-117">-EncryptionKey</span></span>
<span data-ttu-id="f2d6f-118">Verschlüsselungsschlüssel des Edgegeräts</span><span class="sxs-lookup"><span data-stu-id="f2d6f-118">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="f2d6f-119">-Name</span><span class="sxs-lookup"><span data-stu-id="f2d6f-119">-Name</span></span>
<span data-ttu-id="f2d6f-120">Benutzername</span><span class="sxs-lookup"><span data-stu-id="f2d6f-120">Username</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2d6f-121">-Password</span><span class="sxs-lookup"><span data-stu-id="f2d6f-121">-Password</span></span>
<span data-ttu-id="f2d6f-122">Kennwort als sichere Zeichenfolge angeben</span><span class="sxs-lookup"><span data-stu-id="f2d6f-122">Password, provide as a secure string</span></span>

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

### <span data-ttu-id="f2d6f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2d6f-123">-ResourceGroupName</span></span>
<span data-ttu-id="f2d6f-124">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="f2d6f-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2d6f-125">-Type</span><span class="sxs-lookup"><span data-stu-id="f2d6f-125">-Type</span></span>
<span data-ttu-id="f2d6f-126">Select UserType</span><span class="sxs-lookup"><span data-stu-id="f2d6f-126">Select UserType</span></span>

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

### <span data-ttu-id="f2d6f-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f2d6f-127">-Confirm</span></span>
<span data-ttu-id="f2d6f-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f2d6f-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2d6f-129">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="f2d6f-129">-WhatIf</span></span>
<span data-ttu-id="f2d6f-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f2d6f-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f2d6f-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f2d6f-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2d6f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2d6f-132">CommonParameters</span></span>
<span data-ttu-id="f2d6f-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2d6f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2d6f-134">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f2d6f-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2d6f-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f2d6f-135">INPUTS</span></span>

### <span data-ttu-id="f2d6f-136">Keine</span><span class="sxs-lookup"><span data-stu-id="f2d6f-136">None</span></span>

## <span data-ttu-id="f2d6f-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f2d6f-137">OUTPUTS</span></span>

### <span data-ttu-id="f2d6f-138">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="f2d6f-138">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="f2d6f-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f2d6f-139">NOTES</span></span>

## <span data-ttu-id="f2d6f-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f2d6f-140">RELATED LINKS</span></span>

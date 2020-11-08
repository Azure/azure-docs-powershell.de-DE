---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeUser.md
ms.openlocfilehash: a53f67c12a5c8d125319fc19f69db3ea9a57c5e1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173055"
---
# <span data-ttu-id="546db-101">New-AzDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="546db-101">New-AzDataBoxEdgeUser</span></span>

## <span data-ttu-id="546db-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="546db-102">SYNOPSIS</span></span>
<span data-ttu-id="546db-103">Erstellt einen neuen Benutzer für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="546db-103">Creates a new user for the device.</span></span>

## <span data-ttu-id="546db-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="546db-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -Password <SecureString> -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [[-Type] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="546db-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="546db-105">DESCRIPTION</span></span>
<span data-ttu-id="546db-106">Das Cmdlet **New-AzDataBoxEdgeUser** erstellt einen neuen Benutzer für das Daten Feld-Edge-Gerät.</span><span class="sxs-lookup"><span data-stu-id="546db-106">The **New-AzDataBoxEdgeUser** cmdlet creates a new user for the Data Box Edge device.</span></span> <span data-ttu-id="546db-107">Die Erstellung von nur Benutzertypen `Share` wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="546db-107">Creation of only users of type `Share` is supported.</span></span>

## <span data-ttu-id="546db-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="546db-108">EXAMPLES</span></span>

### <span data-ttu-id="546db-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="546db-109">Example 1</span></span>
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

## <span data-ttu-id="546db-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="546db-110">PARAMETERS</span></span>

### <span data-ttu-id="546db-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="546db-111">-AsJob</span></span>
<span data-ttu-id="546db-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="546db-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="546db-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="546db-113">-DefaultProfile</span></span>
<span data-ttu-id="546db-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="546db-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="546db-115">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="546db-115">-DeviceName</span></span>
<span data-ttu-id="546db-116">Geräte Name</span><span class="sxs-lookup"><span data-stu-id="546db-116">Device Name</span></span>

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

### <span data-ttu-id="546db-117">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="546db-117">-EncryptionKey</span></span>
<span data-ttu-id="546db-118">Verschlüsselungsschlüssel des Edge-Geräts</span><span class="sxs-lookup"><span data-stu-id="546db-118">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="546db-119">-Name</span><span class="sxs-lookup"><span data-stu-id="546db-119">-Name</span></span>
<span data-ttu-id="546db-120">Username</span><span class="sxs-lookup"><span data-stu-id="546db-120">Username</span></span>

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

### <span data-ttu-id="546db-121">-Kennwort</span><span class="sxs-lookup"><span data-stu-id="546db-121">-Password</span></span>
<span data-ttu-id="546db-122">Kennwort, als sichere Zeichenfolge bereitstellen</span><span class="sxs-lookup"><span data-stu-id="546db-122">Password, provide as a secure string</span></span>

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

### <span data-ttu-id="546db-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="546db-123">-ResourceGroupName</span></span>
<span data-ttu-id="546db-124">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="546db-124">Resource Group Name</span></span>

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

### <span data-ttu-id="546db-125">-Typ</span><span class="sxs-lookup"><span data-stu-id="546db-125">-Type</span></span>
<span data-ttu-id="546db-126">Benutzertyp auswählen</span><span class="sxs-lookup"><span data-stu-id="546db-126">Select UserType</span></span>

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

### <span data-ttu-id="546db-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="546db-127">-Confirm</span></span>
<span data-ttu-id="546db-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="546db-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="546db-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="546db-129">-WhatIf</span></span>
<span data-ttu-id="546db-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="546db-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="546db-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="546db-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="546db-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="546db-132">CommonParameters</span></span>
<span data-ttu-id="546db-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="546db-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="546db-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="546db-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="546db-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="546db-135">INPUTS</span></span>

### <span data-ttu-id="546db-136">Keine</span><span class="sxs-lookup"><span data-stu-id="546db-136">None</span></span>

## <span data-ttu-id="546db-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="546db-137">OUTPUTS</span></span>

### <span data-ttu-id="546db-138">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="546db-138">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="546db-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="546db-139">NOTES</span></span>

## <span data-ttu-id="546db-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="546db-140">RELATED LINKS</span></span>

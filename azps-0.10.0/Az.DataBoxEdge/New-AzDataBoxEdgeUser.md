---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeUser.md
ms.openlocfilehash: 480c0a8e932b672542595983f33fd19bab6fec3b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844060"
---
# <span data-ttu-id="f1095-101">New-AzDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="f1095-101">New-AzDataBoxEdgeUser</span></span>

## <span data-ttu-id="f1095-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f1095-102">SYNOPSIS</span></span>
<span data-ttu-id="f1095-103">Erstellt einen neuen Benutzer für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="f1095-103">Creates a new user for the device.</span></span>

## <span data-ttu-id="f1095-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f1095-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -Password <SecureString> -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [[-Type] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1095-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f1095-105">DESCRIPTION</span></span>
<span data-ttu-id="f1095-106">Das Cmdlet **New-AzDataBoxEdgeUser** erstellt einen neuen Benutzer für das Daten Feld-Edge-Gerät.</span><span class="sxs-lookup"><span data-stu-id="f1095-106">The **New-AzDataBoxEdgeUser** cmdlet creates a new user for the Data Box Edge device.</span></span> <span data-ttu-id="f1095-107">Die Erstellung von nur Benutzertypen `Share` wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f1095-107">Creation of only users of type `Share` is supported.</span></span>

## <span data-ttu-id="f1095-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f1095-108">EXAMPLES</span></span>

### <span data-ttu-id="f1095-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f1095-109">Example 1</span></span>
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

## <span data-ttu-id="f1095-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f1095-110">PARAMETERS</span></span>

### <span data-ttu-id="f1095-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f1095-111">-AsJob</span></span>
<span data-ttu-id="f1095-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="f1095-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f1095-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1095-113">-DefaultProfile</span></span>
<span data-ttu-id="f1095-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f1095-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1095-115">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="f1095-115">-DeviceName</span></span>
<span data-ttu-id="f1095-116">Geräte Name</span><span class="sxs-lookup"><span data-stu-id="f1095-116">Device Name</span></span>

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

### <span data-ttu-id="f1095-117">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="f1095-117">-EncryptionKey</span></span>
<span data-ttu-id="f1095-118">Verschlüsselungsschlüssel des Edge-Geräts</span><span class="sxs-lookup"><span data-stu-id="f1095-118">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="f1095-119">-Name</span><span class="sxs-lookup"><span data-stu-id="f1095-119">-Name</span></span>
<span data-ttu-id="f1095-120">Username</span><span class="sxs-lookup"><span data-stu-id="f1095-120">Username</span></span>

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

### <span data-ttu-id="f1095-121">-Kennwort</span><span class="sxs-lookup"><span data-stu-id="f1095-121">-Password</span></span>
<span data-ttu-id="f1095-122">Kennwort, als sichere Zeichenfolge bereitstellen</span><span class="sxs-lookup"><span data-stu-id="f1095-122">Password, provide as a secure string</span></span>

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

### <span data-ttu-id="f1095-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1095-123">-ResourceGroupName</span></span>
<span data-ttu-id="f1095-124">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="f1095-124">Resource Group Name</span></span>

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

### <span data-ttu-id="f1095-125">-Typ</span><span class="sxs-lookup"><span data-stu-id="f1095-125">-Type</span></span>
<span data-ttu-id="f1095-126">Benutzertyp auswählen</span><span class="sxs-lookup"><span data-stu-id="f1095-126">Select UserType</span></span>

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

### <span data-ttu-id="f1095-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f1095-127">-Confirm</span></span>
<span data-ttu-id="f1095-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f1095-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1095-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1095-129">-WhatIf</span></span>
<span data-ttu-id="f1095-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f1095-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f1095-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f1095-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1095-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1095-132">CommonParameters</span></span>
<span data-ttu-id="f1095-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1095-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1095-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f1095-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1095-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f1095-135">INPUTS</span></span>

### <span data-ttu-id="f1095-136">Keine</span><span class="sxs-lookup"><span data-stu-id="f1095-136">None</span></span>

## <span data-ttu-id="f1095-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f1095-137">OUTPUTS</span></span>

### <span data-ttu-id="f1095-138">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="f1095-138">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="f1095-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="f1095-139">NOTES</span></span>

## <span data-ttu-id="f1095-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f1095-140">RELATED LINKS</span></span>

---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 35b937b810da65cc3cc2ed330198011ec108f9d6
ms.sourcegitcommit: 10ec909100a70acec94d42f6084e7bf0342c6854
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/19/2020
ms.locfileid: "93847699"
---
# <span data-ttu-id="661c4-101">Restore-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="661c4-101">Restore-AzsBackup</span></span>

## <span data-ttu-id="661c4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="661c4-102">SYNOPSIS</span></span>
<span data-ttu-id="661c4-103">Wiederherstellen einer Sicherung</span><span class="sxs-lookup"><span data-stu-id="661c4-103">Restore a backup.</span></span>

## <span data-ttu-id="661c4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="661c4-104">SYNTAX</span></span>

### <span data-ttu-id="661c4-105">Backups_Restore (Standard)</span><span class="sxs-lookup"><span data-stu-id="661c4-105">Backups_Restore (Default)</span></span>
```
Restore-AzsBackup [-ResourceGroupName <String>] -Name <String> [-Location <String>]
 -DecryptionCertPath <String> -DecryptionCertPassword <SecureString> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="661c4-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="661c4-106">ResourceId</span></span>
```
Restore-AzsBackup -DecryptionCertPath <String> -DecryptionCertPassword <SecureString> -ResourceId <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="661c4-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="661c4-107">DESCRIPTION</span></span>
<span data-ttu-id="661c4-108">Wiederherstellen einer Sicherung</span><span class="sxs-lookup"><span data-stu-id="661c4-108">Restore a backup.</span></span>

## <span data-ttu-id="661c4-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="661c4-109">EXAMPLES</span></span>

### <span data-ttu-id="661c4-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="661c4-110">EXAMPLE 1</span></span>
```
Restore-AzsBackup -Name 4e90bd2f-c7ab-47a3-a3c7-908cddd1ad0e -DecryptionCertPath $decryptionCertPath -DecryptionCertPassword $decryptionCertPassword
```

<span data-ttu-id="661c4-111">Wiederherstellen aus einer Azure Stack-Sicherung</span><span class="sxs-lookup"><span data-stu-id="661c4-111">Restore from an Azure Stack backup.</span></span>

## <span data-ttu-id="661c4-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="661c4-112">PARAMETERS</span></span>

### <span data-ttu-id="661c4-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="661c4-113">-AsJob</span></span>
<span data-ttu-id="661c4-114">Führen Sie asynchron als Auftrag aus, und geben Sie das Auftragsobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="661c4-114">Run asynchronous as a job and return the job object.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="661c4-115">-DecryptionCertPassword</span><span class="sxs-lookup"><span data-stu-id="661c4-115">-DecryptionCertPassword</span></span>
<span data-ttu-id="661c4-116">Kennwort des Entschlüsselungszertifikats.</span><span class="sxs-lookup"><span data-stu-id="661c4-116">Password of the decryption cert.</span></span>

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

### <span data-ttu-id="661c4-117">-DecryptionCertPath</span><span class="sxs-lookup"><span data-stu-id="661c4-117">-DecryptionCertPath</span></span>
<span data-ttu-id="661c4-118">Pfad zur Entschlüsselungs-CERT-Datei mit privatem Schlüssel (PFX).</span><span class="sxs-lookup"><span data-stu-id="661c4-118">Path to the decryption cert file with private key (.pfx).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="661c4-119">-Force</span><span class="sxs-lookup"><span data-stu-id="661c4-119">-Force</span></span>
<span data-ttu-id="661c4-120">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="661c4-120">Don't ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="661c4-121">-Standort</span><span class="sxs-lookup"><span data-stu-id="661c4-121">-Location</span></span>
<span data-ttu-id="661c4-122">Name des zu sichernden Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="661c4-122">Name of location to backup.</span></span>

```yaml
Type: System.String
Parameter Sets: Backups_Restore
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="661c4-123">-Name</span><span class="sxs-lookup"><span data-stu-id="661c4-123">-Name</span></span>
<span data-ttu-id="661c4-124">Der Name der Sicherung.</span><span class="sxs-lookup"><span data-stu-id="661c4-124">Name of the backup.</span></span>

```yaml
Type: System.String
Parameter Sets: Backups_Restore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="661c4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="661c4-125">-ResourceGroupName</span></span>
<span data-ttu-id="661c4-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="661c4-126">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Backups_Restore
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="661c4-127">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="661c4-127">-ResourceId</span></span>
<span data-ttu-id="661c4-128">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="661c4-128">The resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="661c4-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="661c4-129">-Confirm</span></span>
<span data-ttu-id="661c4-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="661c4-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="661c4-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="661c4-131">-WhatIf</span></span>
<span data-ttu-id="661c4-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="661c4-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="661c4-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="661c4-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="661c4-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="661c4-134">CommonParameters</span></span>
<span data-ttu-id="661c4-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="661c4-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="661c4-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="661c4-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="661c4-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="661c4-137">INPUTS</span></span>

## <span data-ttu-id="661c4-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="661c4-138">OUTPUTS</span></span>

## <span data-ttu-id="661c4-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="661c4-139">NOTES</span></span>

## <span data-ttu-id="661c4-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="661c4-140">RELATED LINKS</span></span>

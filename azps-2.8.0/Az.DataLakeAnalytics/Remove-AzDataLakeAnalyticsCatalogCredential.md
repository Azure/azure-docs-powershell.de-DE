---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: C6BB6E4D-6009-4796-866B-17115FDFA06D
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticscatalogcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsCatalogCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsCatalogCredential.md
ms.openlocfilehash: 79e5823c797c878643ea6ad2870873da363d0312
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651606"
---
# <span data-ttu-id="02c12-101">Remove-AzDataLakeAnalyticsCatalogCredential</span><span class="sxs-lookup"><span data-stu-id="02c12-101">Remove-AzDataLakeAnalyticsCatalogCredential</span></span>

## <span data-ttu-id="02c12-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="02c12-102">SYNOPSIS</span></span>
<span data-ttu-id="02c12-103">Löscht eine Azure Data Lake-Analyse Anmeldeinformationen.</span><span class="sxs-lookup"><span data-stu-id="02c12-103">Deletes an Azure Data Lake Analytics credential.</span></span>

## <span data-ttu-id="02c12-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="02c12-104">SYNTAX</span></span>

```
Remove-AzDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String> [-Name] <String>
 [[-Password] <PSCredential>] [-Recurse] [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02c12-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="02c12-105">DESCRIPTION</span></span>
<span data-ttu-id="02c12-106">Das Remove-AzDataLakeAnalyticsCatalogCredential-Cmdlet löscht eine Azure Data Lake Analytics-Katalog Anmeldeinformationen.</span><span class="sxs-lookup"><span data-stu-id="02c12-106">The Remove-AzDataLakeAnalyticsCatalogCredential cmdlet deletes an Azure Data Lake Analytics catalog credential.</span></span>

## <span data-ttu-id="02c12-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="02c12-107">EXAMPLES</span></span>

### <span data-ttu-id="02c12-108">Beispiel 1: Entfernen von Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="02c12-108">Example 1: Remove a credential</span></span>
```
PS C:\> Remove-AzDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdla" `
                      -DatabaseName "DatabaseName" `
                      -Name "CredName"
```

<span data-ttu-id="02c12-109">Mit diesem Befehl werden die Anmeldeinformationen für den angegebenen Data Lake Analytics-Katalog entfernt.</span><span class="sxs-lookup"><span data-stu-id="02c12-109">This command removes the specified Data Lake Analytics catalog credential.</span></span>

## <span data-ttu-id="02c12-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="02c12-110">PARAMETERS</span></span>

### <span data-ttu-id="02c12-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="02c12-111">-Account</span></span>
<span data-ttu-id="02c12-112">Gibt den Namen des Daten Lake Analytics-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="02c12-112">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02c12-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="02c12-113">-DatabaseName</span></span>
<span data-ttu-id="02c12-114">Gibt den Namen der Datenbank an, die die Anmeldeinformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="02c12-114">Specifies the name of the database that holds the credential.</span></span>

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

### <span data-ttu-id="02c12-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02c12-115">-DefaultProfile</span></span>
<span data-ttu-id="02c12-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="02c12-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="02c12-117">-Force</span><span class="sxs-lookup"><span data-stu-id="02c12-117">-Force</span></span>
<span data-ttu-id="02c12-118">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="02c12-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="02c12-119">-Name</span><span class="sxs-lookup"><span data-stu-id="02c12-119">-Name</span></span>
<span data-ttu-id="02c12-120">Gibt den Namen der Anmeldeinformationen an.</span><span class="sxs-lookup"><span data-stu-id="02c12-120">Specifies the name of the credential.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02c12-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="02c12-121">-PassThru</span></span>
<span data-ttu-id="02c12-122">Gibt an, dass dieses Cmdlet nicht wartet, bis der Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="02c12-122">Indicates that this cmdlet does not wait for the operation to complete.</span></span>
<span data-ttu-id="02c12-123">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="02c12-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="02c12-124">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="02c12-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="02c12-125">-Kennwort</span><span class="sxs-lookup"><span data-stu-id="02c12-125">-Password</span></span>
<span data-ttu-id="02c12-126">Das Kennwort für die Anmeldeinformationen.</span><span class="sxs-lookup"><span data-stu-id="02c12-126">The password for the credential.</span></span>
<span data-ttu-id="02c12-127">Dies ist erforderlich, wenn der Anrufer nicht der Besitzer des Kontos ist.</span><span class="sxs-lookup"><span data-stu-id="02c12-127">This is required if the caller is not the owner of the account.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02c12-128">-Rekursiv</span><span class="sxs-lookup"><span data-stu-id="02c12-128">-Recurse</span></span>
<span data-ttu-id="02c12-129">Gibt an, dass dieser Löschvorgang durchlaufen und auch alle Ressourcen, die von diesen Anmeldeinformationen abhängig sind, gelöscht und gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="02c12-129">Indicates that this delete operation should go through and also delete and drop all resources dependent on this credential.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02c12-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="02c12-130">-Confirm</span></span>
<span data-ttu-id="02c12-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="02c12-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02c12-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02c12-132">-WhatIf</span></span>
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

### <span data-ttu-id="02c12-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02c12-133">CommonParameters</span></span>
<span data-ttu-id="02c12-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02c12-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02c12-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02c12-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02c12-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="02c12-136">INPUTS</span></span>

### <span data-ttu-id="02c12-137">System. String</span><span class="sxs-lookup"><span data-stu-id="02c12-137">System.String</span></span>

### <span data-ttu-id="02c12-138">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="02c12-138">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="02c12-139">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="02c12-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="02c12-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="02c12-140">OUTPUTS</span></span>

### <span data-ttu-id="02c12-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="02c12-141">System.Boolean</span></span>

## <span data-ttu-id="02c12-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="02c12-142">NOTES</span></span>

## <span data-ttu-id="02c12-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="02c12-143">RELATED LINKS</span></span>

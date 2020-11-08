---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: C6BB6E4D-6009-4796-866B-17115FDFA06D
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticscatalogcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsCatalogCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsCatalogCredential.md
ms.openlocfilehash: 9fbc00fe190e0a53fc9c41a6894ec35a7f8d9129
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008073"
---
# <span data-ttu-id="e9c52-101">Remove-AzDataLakeAnalyticsCatalogCredential</span><span class="sxs-lookup"><span data-stu-id="e9c52-101">Remove-AzDataLakeAnalyticsCatalogCredential</span></span>

## <span data-ttu-id="e9c52-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e9c52-102">SYNOPSIS</span></span>
<span data-ttu-id="e9c52-103">Löscht eine Azure Data Lake-Analyse Anmeldeinformationen.</span><span class="sxs-lookup"><span data-stu-id="e9c52-103">Deletes an Azure Data Lake Analytics credential.</span></span>

## <span data-ttu-id="e9c52-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e9c52-104">SYNTAX</span></span>

```
Remove-AzDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String> [-Name] <String>
 [[-Password] <PSCredential>] [-Recurse] [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9c52-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e9c52-105">DESCRIPTION</span></span>
<span data-ttu-id="e9c52-106">Das Remove-AzDataLakeAnalyticsCatalogCredential-Cmdlet löscht eine Azure Data Lake Analytics-Katalog Anmeldeinformationen.</span><span class="sxs-lookup"><span data-stu-id="e9c52-106">The Remove-AzDataLakeAnalyticsCatalogCredential cmdlet deletes an Azure Data Lake Analytics catalog credential.</span></span>

## <span data-ttu-id="e9c52-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e9c52-107">EXAMPLES</span></span>

### <span data-ttu-id="e9c52-108">Beispiel 1: Entfernen von Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="e9c52-108">Example 1: Remove a credential</span></span>
```
PS C:\> Remove-AzDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdla" `
                      -DatabaseName "DatabaseName" `
                      -Name "CredName"
```

<span data-ttu-id="e9c52-109">Mit diesem Befehl werden die Anmeldeinformationen für den angegebenen Data Lake Analytics-Katalog entfernt.</span><span class="sxs-lookup"><span data-stu-id="e9c52-109">This command removes the specified Data Lake Analytics catalog credential.</span></span>

## <span data-ttu-id="e9c52-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e9c52-110">PARAMETERS</span></span>

### <span data-ttu-id="e9c52-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="e9c52-111">-Account</span></span>
<span data-ttu-id="e9c52-112">Gibt den Namen des Daten Lake Analytics-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="e9c52-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="e9c52-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e9c52-113">-DatabaseName</span></span>
<span data-ttu-id="e9c52-114">Gibt den Namen der Datenbank an, die die Anmeldeinformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="e9c52-114">Specifies the name of the database that holds the credential.</span></span>

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

### <span data-ttu-id="e9c52-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9c52-115">-DefaultProfile</span></span>
<span data-ttu-id="e9c52-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="e9c52-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e9c52-117">-Force</span><span class="sxs-lookup"><span data-stu-id="e9c52-117">-Force</span></span>
<span data-ttu-id="e9c52-118">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="e9c52-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e9c52-119">-Name</span><span class="sxs-lookup"><span data-stu-id="e9c52-119">-Name</span></span>
<span data-ttu-id="e9c52-120">Gibt den Namen der Anmeldeinformationen an.</span><span class="sxs-lookup"><span data-stu-id="e9c52-120">Specifies the name of the credential.</span></span>

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

### <span data-ttu-id="e9c52-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e9c52-121">-PassThru</span></span>
<span data-ttu-id="e9c52-122">Gibt an, dass dieses Cmdlet nicht wartet, bis der Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="e9c52-122">Indicates that this cmdlet does not wait for the operation to complete.</span></span>
<span data-ttu-id="e9c52-123">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="e9c52-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e9c52-124">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="e9c52-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e9c52-125">-Kennwort</span><span class="sxs-lookup"><span data-stu-id="e9c52-125">-Password</span></span>
<span data-ttu-id="e9c52-126">Das Kennwort für die Anmeldeinformationen.</span><span class="sxs-lookup"><span data-stu-id="e9c52-126">The password for the credential.</span></span>
<span data-ttu-id="e9c52-127">Dies ist erforderlich, wenn der Anrufer nicht der Besitzer des Kontos ist.</span><span class="sxs-lookup"><span data-stu-id="e9c52-127">This is required if the caller is not the owner of the account.</span></span>

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

### <span data-ttu-id="e9c52-128">-Rekursiv</span><span class="sxs-lookup"><span data-stu-id="e9c52-128">-Recurse</span></span>
<span data-ttu-id="e9c52-129">Gibt an, dass dieser Löschvorgang durchlaufen und auch alle Ressourcen, die von diesen Anmeldeinformationen abhängig sind, gelöscht und gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="e9c52-129">Indicates that this delete operation should go through and also delete and drop all resources dependent on this credential.</span></span>

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

### <span data-ttu-id="e9c52-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e9c52-130">-Confirm</span></span>
<span data-ttu-id="e9c52-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e9c52-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9c52-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9c52-132">-WhatIf</span></span>
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

### <span data-ttu-id="e9c52-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9c52-133">CommonParameters</span></span>
<span data-ttu-id="e9c52-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9c52-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9c52-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9c52-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9c52-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e9c52-136">INPUTS</span></span>

### <span data-ttu-id="e9c52-137">System. String</span><span class="sxs-lookup"><span data-stu-id="e9c52-137">System.String</span></span>

### <span data-ttu-id="e9c52-138">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="e9c52-138">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="e9c52-139">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="e9c52-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e9c52-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e9c52-140">OUTPUTS</span></span>

### <span data-ttu-id="e9c52-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e9c52-141">System.Boolean</span></span>

## <span data-ttu-id="e9c52-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="e9c52-142">NOTES</span></span>

## <span data-ttu-id="e9c52-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e9c52-143">RELATED LINKS</span></span>

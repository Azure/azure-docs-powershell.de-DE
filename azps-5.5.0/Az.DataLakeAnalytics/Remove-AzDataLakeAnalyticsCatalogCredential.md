---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: C6BB6E4D-6009-4796-866B-17115FDFA06D
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticscatalogcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsCatalogCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsCatalogCredential.md
ms.openlocfilehash: 9fbc00fe190e0a53fc9c41a6894ec35a7f8d9129
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100162041"
---
# <span data-ttu-id="0f5e9-101">Remove-AzDataLakeAnalyticsCatalogCredential</span><span class="sxs-lookup"><span data-stu-id="0f5e9-101">Remove-AzDataLakeAnalyticsCatalogCredential</span></span>

## <span data-ttu-id="0f5e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f5e9-102">SYNOPSIS</span></span>
<span data-ttu-id="0f5e9-103">Löscht eine Azure Data Lake Analytics-Anmeldeinformationen.</span><span class="sxs-lookup"><span data-stu-id="0f5e9-103">Deletes an Azure Data Lake Analytics credential.</span></span>

## <span data-ttu-id="0f5e9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0f5e9-104">SYNTAX</span></span>

```
Remove-AzDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String> [-Name] <String>
 [[-Password] <PSCredential>] [-Recurse] [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f5e9-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0f5e9-105">DESCRIPTION</span></span>
<span data-ttu-id="0f5e9-106">Das Remove-AzDataLakeAnalyticsCatalogCredential cmdlet löscht die Anmeldeinformationen eines Azure Data Lake Analytics-Katalogs.</span><span class="sxs-lookup"><span data-stu-id="0f5e9-106">The Remove-AzDataLakeAnalyticsCatalogCredential cmdlet deletes an Azure Data Lake Analytics catalog credential.</span></span>

## <span data-ttu-id="0f5e9-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0f5e9-107">EXAMPLES</span></span>

### <span data-ttu-id="0f5e9-108">Beispiel 1: Entfernen von Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="0f5e9-108">Example 1: Remove a credential</span></span>
```
PS C:\> Remove-AzDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdla" `
                      -DatabaseName "DatabaseName" `
                      -Name "CredName"
```

<span data-ttu-id="0f5e9-109">Mit diesem Befehl werden die angegebenen Data Lake Analytics-Kataloganmeldeinformationen entfernt.</span><span class="sxs-lookup"><span data-stu-id="0f5e9-109">This command removes the specified Data Lake Analytics catalog credential.</span></span>

## <span data-ttu-id="0f5e9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0f5e9-110">PARAMETERS</span></span>

### <span data-ttu-id="0f5e9-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="0f5e9-111">-Account</span></span>
<span data-ttu-id="0f5e9-112">Gibt den Namen des Data Lake Analytics-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="0f5e9-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="0f5e9-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0f5e9-113">-DatabaseName</span></span>
<span data-ttu-id="0f5e9-114">Gibt den Namen der Datenbank an, die die Anmeldeinformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="0f5e9-114">Specifies the name of the database that holds the credential.</span></span>

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

### <span data-ttu-id="0f5e9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f5e9-115">-DefaultProfile</span></span>
<span data-ttu-id="0f5e9-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="0f5e9-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0f5e9-117">-Force</span><span class="sxs-lookup"><span data-stu-id="0f5e9-117">-Force</span></span>
<span data-ttu-id="0f5e9-118">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="0f5e9-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0f5e9-119">-Name</span><span class="sxs-lookup"><span data-stu-id="0f5e9-119">-Name</span></span>
<span data-ttu-id="0f5e9-120">Gibt den Namen der Anmeldeinformationen an.</span><span class="sxs-lookup"><span data-stu-id="0f5e9-120">Specifies the name of the credential.</span></span>

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

### <span data-ttu-id="0f5e9-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0f5e9-121">-PassThru</span></span>
<span data-ttu-id="0f5e9-122">Gibt an, dass dieses Cmdlet nicht auf den Abschluss des Vorgangs wartet.</span><span class="sxs-lookup"><span data-stu-id="0f5e9-122">Indicates that this cmdlet does not wait for the operation to complete.</span></span>
<span data-ttu-id="0f5e9-123">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="0f5e9-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0f5e9-124">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="0f5e9-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0f5e9-125">-Password</span><span class="sxs-lookup"><span data-stu-id="0f5e9-125">-Password</span></span>
<span data-ttu-id="0f5e9-126">Das Kennwort für die Anmeldeinformationen.</span><span class="sxs-lookup"><span data-stu-id="0f5e9-126">The password for the credential.</span></span>
<span data-ttu-id="0f5e9-127">Dies ist erforderlich, wenn der Anrufer nicht der Besitzer des Kontos ist.</span><span class="sxs-lookup"><span data-stu-id="0f5e9-127">This is required if the caller is not the owner of the account.</span></span>

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

### <span data-ttu-id="0f5e9-128">-Recurse</span><span class="sxs-lookup"><span data-stu-id="0f5e9-128">-Recurse</span></span>
<span data-ttu-id="0f5e9-129">Gibt an, dass dieser Löschvorgang durchgehen und auch alle Ressourcen löschen und löschen soll, die von diesen Anmeldeinformationen abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="0f5e9-129">Indicates that this delete operation should go through and also delete and drop all resources dependent on this credential.</span></span>

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

### <span data-ttu-id="0f5e9-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0f5e9-130">-Confirm</span></span>
<span data-ttu-id="0f5e9-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0f5e9-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f5e9-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="0f5e9-132">-WhatIf</span></span>
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

### <span data-ttu-id="0f5e9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f5e9-133">CommonParameters</span></span>
<span data-ttu-id="0f5e9-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f5e9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f5e9-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f5e9-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f5e9-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0f5e9-136">INPUTS</span></span>

### <span data-ttu-id="0f5e9-137">System.String</span><span class="sxs-lookup"><span data-stu-id="0f5e9-137">System.String</span></span>

### <span data-ttu-id="0f5e9-138">System.Management.Automation.PSCredential</span><span class="sxs-lookup"><span data-stu-id="0f5e9-138">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="0f5e9-139">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="0f5e9-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0f5e9-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0f5e9-140">OUTPUTS</span></span>

### <span data-ttu-id="0f5e9-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0f5e9-141">System.Boolean</span></span>

## <span data-ttu-id="0f5e9-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0f5e9-142">NOTES</span></span>

## <span data-ttu-id="0f5e9-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0f5e9-143">RELATED LINKS</span></span>
